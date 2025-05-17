# Define acceptable tolerance range
TARGET_LENGTH = 100.0   # mm
TOLERANCE = 2.0         # mm

# Sample data: Lengths of manufactured items (in mm)
measured_lengths = [99.8, 100.5, 101.2, 98.9, 97.5, 100.1, 103.0]

def is_within_tolerance(length, target, tolerance):
    return abs(length - target) <= tolerance

def quality_control_report(measurements):
    passed = []
    failed = []
    for i, length in enumerate(measurements, start=1):
        if is_within_tolerance(length, TARGET_LENGTH, TOLERANCE):
            passed.append((i, length))
        else:
            failed.append((i, length))

    print("Quality Control Report")
    print("----------------------")
    print(f"Target Length: {TARGET_LENGTH} mm ± {TOLERANCE} mm\n")

    print("Passed Items:")
    for item in passed:
        print(f"Item {item[0]}: {item[1]} mm")

    print("\nFailed Items:")
    for item in failed:
        print(f"Item {item[0]}: {item[1]} mm")

# Run the report
quality_control_report(measured_lengths)

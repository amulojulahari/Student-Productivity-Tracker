# Fix Warnings and Errors in activity_main.xml

This plan addresses layout issues, hardcoded strings, and missing/invalid constraints in `activity_main.xml`.

## Proposed Changes

### Layout Optimization

#### [MODIFY] [activity_main.xml](file:///C:/Users/alaha/AndroidStudioProjects/StudentTaskManager2/app/src/main/res/layout/activity_main.xml)
- Change root `ConstraintLayout` `android:layout_width` from `wrap_content` to `match_parent`.
- Add `android:id="@+id/textView1"` to the first `TextView`.
- Fix the first `TextView` constraints to be properly centered if that was the intent, or remove conflicting margins.
- Fix `textView3` constraints: `app:layout_constraintStart_toEndOf="parent"` is invalid for visibility; change to `app:layout_constraintEnd_toEndOf="parent"` or `app:layout_constraintStart_toStartOf="parent"`.
- Extract hardcoded strings `"TextView"` to `strings.xml`.

### Resource Management

#### [MODIFY] [strings.xml](file:///C:/Users/alaha/AndroidStudioProjects/StudentTaskManager2/app/src/main/res/values/strings.xml)
- Add string resources for the `TextView` labels.

## Verification Plan

### Manual Verification
- Use the layout editor/preview to ensure all views are visible and correctly positioned.
- Check for any remaining lint warnings in the IDE.

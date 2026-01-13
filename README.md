TaskGlitch - SDE Bug Fix Challenge

Project Overview This Task Management Application is designed for sales teams to track, manage, and prioritize tasks based on ROI. The goal of this assignment was to transform a glitchy application into a stable tool by fixing logic errors, UI inconsistencies, and performance issues.

Live Demo: https://the-task-glitch-challenge-erino-dep-eight.vercel.app/

Bug Fix Documentation

1. Double Fetch Issue

Issue: The task retrieval function was running twice on page load, causing duplicate data.

Fix: Analyzed the useTasks hook and removed a redundant useEffect block that was intentionally injecting duplicate data.

2. Undo Snackbar Logic

Issue: The Undo feature retained the deleted task state even after the notification closed, allowing users to restore incorrect items later.

Fix: Implemented a dismissUndo function and connected it to the Snackbar's close handler to reset the deleted state immediately upon closing.

3. Unstable Sorting

Issue: Tasks with identical ROI values caused the list to flicker because the sort order was random.

Fix: Updated the sorting logic to use the Task Title as a deterministic tie-breaker, ensuring a stable order.

4. Double Dialog Opening

Issue: Clicking Edit or Delete buttons triggered both the specific action and the row's View Details dialog.

Fix: Added stopPropagation to the click handlers for both the Edit and Delete buttons to prevent event bubbling.

5. ROI Calculation Errors

Issue: Tasks with zero hours or missing data displayed Infinity or NaN errors.


Video Url Link:  https://drive.google.com/file/d/1ZM4AlTnctO73WLqX4o26rh6D6uNo1eS_/view?usp=sharing

---
UID: NF:winuser.RegisterForTooltipDismissNotification
tech.root: inputdev
title: RegisterForTooltipDismissNotification
ms.date: 06/17/2022
targetos: Windows
description: Lets apps or UI frameworks register and unregister windows to receive notification to dismiss their tooltip windows.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winuser.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: user32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - RegisterForTooltipDismissNotification
f1_keywords:
 - RegisterForTooltipDismissNotification
 - winuser/RegisterForTooltipDismissNotification
dev_langs:
 - c++
helpviewer_keywords:
 - RegisterForTooltipDismissNotification
---

## -description

Registers or unregisters windows to receive notification to dismiss their tooltip windows.

## -parameters

### -param hWnd

Type: **HWND**

The handle of the window to receive the **WM_TOOLTIPDISMISS** message.

### -param tdFlags

Type: **[TOOLTIP_DISMISS_FLAGS](ne-winuser-tooltip_dismiss_flags.md)**

A value of the enumeration that specifies whether the function registers or unregisters the window. **TDF_REGISTER** to register; **TDF_UNREGISTER** to unregister.

## -returns

**TRUE** if the window was successfully registered or unregistered; otherwise, **FALSE**. (See Remarks.)

## -remarks

This function makes tooltips more accessible by letting apps and frameworks that support tooltips register and unregister to be notified by a **WM_TOOLTIPDISMISS** message when the system requires all showing tooltips to be dismissed.

Apps should register for this notification each time they show a tooltip and hide their tooltips in response to a **WM_TOOLTIPDISMISS** message. When a tooltip is hidden for some other reason, like a mouse action, the app should unregister.

System-defined triggers for tooltip dismissal include a solitary Ctrl key up or Ctrl+Shift+F10. (The set of triggers may change over time.)

The function takes either the **HWND** of a tooltip window or the **HWND** of an app window that has child tooltips.  

- If a tooltip **HWND** itself is registered, the tooltip window is expected to register upon showing and to dismiss upon receiving a **WM_TOOLTIPDISMISS** message.  
- If an app **HWND** registers on behalf of its tooltips, the app's window is expected to register upon showing tooltips and dismiss all of its tooltips upon receiving a **WM_TOOLTIPDISMISS** message.  

Tooltip or app windows are expected to call the function to register each time tooltips are shown. Registered windows are automatically unregistered upon posting **WM_TOOLTIPDISMISS**.

The **TDF_UNREGISTER** flag is used to explicitly unregister a window when a tooltip window is dismissed by application or framework prerogative (such as moving the cursor out of the "safe zone"). If an app or framework calls `RegisterForTooltipDismissNotification` with **TDF_UNREGISTER** after the window has been automatically unregistered, the function returns **FALSE**. There is no impact on future registrations.

### Return values

The HWND passed into the function must be owned by the calling process; otherwise, the function returns **FALSE**.

When called with **TDF_REGISTER** and a window belonging to the calling process, the function returns **TRUE** if the window was successfully registered or **FALSE** if the window was already registered. The window is treated as registered either way.

When called with **TDF_UNREGISTER** and a windows belonging to the calling process, the function returns **TRUE** if the window is successfully unregistered, or **FALSE** if the windows was not currently registered. The window is treated as unregistered either way.

## -see-also

[Tooltip](/windows/win32/controls/tooltip-control-reference)

## Examples

```cpp
// WndProc: Window procedure for a window that is the parent of one or more 
// tooltip windows. 
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    switch (message) 
    { 
    case WM_TOOLTIPDISMISS: 
        // System is asking us to dismiss tooltip window due to system hotkey. 
        if (hwndVisibleTooltip) 
        { 
            // Hide the tooltip window. Not necessary to unregister as window is 
            // automatically unregistered upon notification. 
            ShowWindow(hwndVisibleTooltip, SW_HIDE); 
            hwndVisibleTooltip = nullptr; 
        } 
        break; 
    case WM_NOTIFY: 
        { 
            LPNMHDR toolInfo = (LPNMHDR) lParam; 
            switch (toolInfo->code) 
            { 
            case TTN_SHOW: 
                // Notification that a tooltip is about to show. Register this 
                // window to receive dismiss notification when the system wants 
                // to dismiss tooltips (such as in response to a system hotkey). 
                RegisterForTooltipDismissNotification(hWnd, TDF_REGISTER); 
 
                // Remember the visible tooltip window, so we know which one to 
                // hide when we receive WM_TOOLTIPTISMISS. 
                hwndVisibleTooltip = toolInfo->hwndFrom; 
                break; 
            case TTN_POP: 
                // Notification that a tooltip is about to hide 
                if (hwndVisibleTooltip) 
                { 
                    // With the tooltip hiding, we will no longer need the system 
                    // dismiss notification, so we can unregister from it. 
                    RegisterForTooltipDismissNotification(hWnd, TDF_UNREGISTER); 
                    hwndVisibleTooltip = nullptr; 
                } 
                break; 
            default: 
                return DefWindowProc(hWnd, message, wParam, lParam); 
            } 
        } 
        break; 
    case WM_DESTROY: 
        PostQuitMessage(0); 
        break; 
    default: 
        return DefWindowProc(hWnd, message, wParam, lParam); 
    } 
    return 0; 
}
```

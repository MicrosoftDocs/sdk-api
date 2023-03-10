---
UID: NF:oleacc.AccNotifyTouchInteraction
title: AccNotifyTouchInteraction function (oleacc.h)
description: Allows an assistive technology (AT) application to notify the system that it is interacting with UI through a Windows Automation API (such as Microsoft UI Automation) as a result of a touch gesture from the user.
helpviewer_keywords: ["AccNotifyTouchInteraction","AccNotifyTouchInteraction function [Windows Accessibility]","oleacc/AccNotifyTouchInteraction","winauto.accnotifytouchinteraction"]
old-location: winauto\accnotifytouchinteraction.htm
tech.root: WinAuto
ms.assetid: CB533913-95A7-45D5-B0D3-E931E4F73B2E
ms.date: 12/05/2018
ms.keywords: AccNotifyTouchInteraction, AccNotifyTouchInteraction function [Windows Accessibility], oleacc/AccNotifyTouchInteraction, winauto.accnotifytouchinteraction
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AccNotifyTouchInteraction
 - oleacc/AccNotifyTouchInteraction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - AccNotifyTouchInteraction
---

# AccNotifyTouchInteraction function


## -description

Allows an assistive technology (AT) application to notify the system that it is interacting with UI through a Windows Automation API (such as Microsoft UI Automation) as a result of a touch gesture from the user. This allows the assistive technology to notify the target application and the system that the user is interacting with touch.

## -parameters

### -param hwndApp [in]

A window that belongs to the AT process that is calling <b>AccNotifyTouchInteraction</b>.

### -param hwndTarget [in]

The nearest window of the automation element that the AT is targeting.

### -param ptTarget [in]

The center point of the automation element (or a point in the bounding rectangle of the element).

## -returns

If successful, returns S_OK.

If not successful, returns a standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.

## -remarks

This function requires the calling process to have UIAccess or higher privileges.  If the caller does not have the required privileges, the call to <b>AccNotifyTouchInteraction</b> fails and returns <b>E_ACCESSDENIED</b>. For more information, see <a href="/windows/desktop/WinAuto/uiauto-securityoverview">Security Considerations for Assistive Technologies</a> and <a href="/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest">/MANIFESTUAC (Embeds UAC information in manifest)</a>.

When an AT is consuming touch data (such as when using the <a href="/windows/desktop/api/winuser/nf-winuser-registerpointerinputtarget">RegisterPointerInputTarget</a> function), the shell and applications that the AT interacts with through the Windows Automation API are not aware that the user is interacting through touch. For the system to expose touch-related functionality to the user, the AT must use <b>AccNotifyTouchInteraction</b> to notify the system that it is performing the interaction in response to user touch input.


#### Examples

This code example shows how to call the <b>AccNotifyTouchInteraction</b> function. 


```cpp
// pTargetElement is the element being interacted with by the user, hwndApp 
// represents an HWND owned by the AT.
HRESULT PerformTouchBasedInteraction(IUIAutomationElement *pTargetElement, 
        HWND hwndApp)
{
    HRESULT hr = S_OK;

    // Set the focus to the element and then notify the system that the 
    // interaction is occurring due to a touch gesture. This would also apply 
    // to pattern-based interactions (such as calls to 
    // IUIAutomationInvokePattern::Invoke)
    hr = pTargetElement->SetFocus();
    if (SUCCEEDED(hr))
    {
        HWND hwndTarget;
        POINT ptTarget;
        BOOL fGotClickablePoint;

        // If the current element does not have a native window handle, an 
        // alternate method (such as walking up the parent chain) is required 
        // to get the nearest valid HWND.
        hr = pTargetElement->get_CurrentNativeWindowHandle((UIA_HWND *)(&hwndTarget));
        if (SUCCEEDED(hr))
        {
            // If the provider doesn't return a clickable point, an alternate 
            // method (such as using the bounding rectangle) will be required 
            // to get the center point of the current element.
            hr = pTargetElement->GetClickablePoint(&ptTarget, &fGotClickablePoint);
        }

        if (SUCCEEDED(hr) && fGotClickablePoint)
        {
            hr = AccNotifyTouchInteraction(hwndApp, hwndTarget, ptTarget);
        }
    }

    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-accsetrunningutilitystate">AccSetRunningUtilityState</a>



<a href="/windows/desktop/api/winuser/nf-winuser-registerpointerinputtarget">RegisterPointerInputTarget</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unregisterpointerinputtarget">UnregisterPointerInputTarget</a>
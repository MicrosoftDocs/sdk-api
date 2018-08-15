---
UID: NF:oleacc.AccNotifyTouchInteraction
title: AccNotifyTouchInteraction function
author: windows-sdk-content
description: Allows an assistive technology (AT) application to notify the system that it is interacting with UI through a Windows Automation API (such as Microsoft UI Automation) as a result of a touch gesture from the user.
old-location: winauto\accnotifytouchinteraction.htm
old-project: WinAuto
ms.assetid: CB533913-95A7-45D5-B0D3-E931E4F73B2E
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AccNotifyTouchInteraction, AccNotifyTouchInteraction function [Windows Accessibility], oleacc/AccNotifyTouchInteraction, winauto.accnotifytouchinteraction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleacc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - AccNotifyTouchInteraction
product: Windows
targetos: Windows
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
req.product: ADAM
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

If not successful, returns a standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.




## -remarks



This function requires the calling process to have UIAccess or higher privileges.  If the caller does not have the required privileges, the call to <b>AccNotifyTouchInteraction</b> fails and returns <b>E_ACCESSDENIED</b>. For more information, see <a href="https://msdn.microsoft.com/0c3689e1-2124-4142-b0bd-233e95ee1285">Security Considerations for Assistive Technologies</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=207612">/MANIFESTUAC (Embeds UAC information in manifest)</a>.

When an AT is consuming touch data (such as when using the <a href="https://msdn.microsoft.com/75faea24-91cd-448b-b67a-09fe530f1830">RegisterPointerInputTarget</a> function), the shell and applications that the AT interacts with through the Windows Automation API are not aware that the user is interacting through touch. For the system to expose touch-related functionality to the user, the AT must use <b>AccNotifyTouchInteraction</b> to notify the system that it is performing the interaction in response to user touch input.


#### Examples

This code example shows how to call the <b>AccNotifyTouchInteraction</b> function. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// pTargetElement is the element being interacted with by the user, hwndApp 
// represents an HWND owned by the AT.
HRESULT PerformTouchBasedInteraction(IUIAutomationElement *pTargetElement, 
        HWND hwndApp)
{
    HRESULT hr = S_OK;

    // Set the focus to the element and then notify the system that the 
    // interaction is occurring due to a touch gesture. This would also apply 
    // to pattern-based interactions (such as calls to 
    // IUIAutomationInvokePattern::Invoke)
    hr = pTargetElement-&gt;SetFocus();
    if (SUCCEEDED(hr))
    {
        HWND hwndTarget;
        POINT ptTarget;
        BOOL fGotClickablePoint;

        // If the current element does not have a native window handle, an 
        // alternate method (such as walking up the parent chain) is required 
        // to get the nearest valid HWND.
        hr = pTargetElement-&gt;get_CurrentNativeWindowHandle((UIA_HWND *)(&amp;hwndTarget));
        if (SUCCEEDED(hr))
        {
            // If the provider doesn't return a clickable point, an alternate 
            // method (such as using the bounding rectangle) will be required 
            // to get the center point of the current element.
            hr = pTargetElement-&gt;GetClickablePoint(&amp;ptTarget, &amp;fGotClickablePoint);
        }

        if (SUCCEEDED(hr) &amp;&amp; fGotClickablePoint)
        {
            hr = AccNotifyTouchInteraction(hwndApp, hwndTarget, ptTarget);
        }
    }

    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0AEDDE0D-D8E2-4C9E-AB2B-2FF0ACC3695D">AccSetRunningUtilityState</a>



<a href="https://msdn.microsoft.com/75faea24-91cd-448b-b67a-09fe530f1830">RegisterPointerInputTarget</a>



<a href="https://msdn.microsoft.com/75faea24-91cd-448b-b67a-09fe530f1800">UnregisterPointerInputTarget</a>
 

 


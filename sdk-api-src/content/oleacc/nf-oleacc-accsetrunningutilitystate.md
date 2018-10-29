---
UID: NF:oleacc.AccSetRunningUtilityState
title: AccSetRunningUtilityState function
author: windows-sdk-content
description: Sets system values that indicate whether an assistive technology (AT) application's current state affects functionality that is typically provided by the system.
old-location: winauto\accsetrunningutilitystate.htm
tech.root: WinAuto
ms.assetid: 0AEDDE0D-D8E2-4C9E-AB2B-2FF0ACC3695D
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ANRUS_ON_SCREEN_KEYBOARD_ACTIVE, ANRUS_PRIORITY_AUDIO_ACTIVE, ANRUS_PRIORITY_AUDIO_ACTIVE_NODUCK, ANRUS_TOUCH_MODIFICATION_ACTIVE, AccSetRunningUtilityState, AccSetRunningUtilityState function [Windows Accessibility], oleacc/AccSetRunningUtilityState, winauto.accsetrunningutilitystate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - AccSetRunningUtilityState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AccSetRunningUtilityState function


## -description


Sets system values that indicate whether an assistive technology (AT) application's current state  affects  functionality that is typically provided by the system. 


## -parameters




### -param hwndApp [in]

Type: <b>HWND</b>

The handle of the AT application window. This parameter must not be <b>NULL</b>.


### -param dwUtilityStateMask [in]

Type: <b>DWORD</b>


A  
mask that indicates the system values being set. It can be a combination of the following values:



<a id="ANRUS_ON_SCREEN_KEYBOARD_ACTIVE"></a>
<a id="anrus_on_screen_keyboard_active"></a>


#### ANRUS_ON_SCREEN_KEYBOARD_ACTIVE

<a id="ANRUS_TOUCH_MODIFICATION_ACTIVE"></a>
<a id="anrus_touch_modification_active"></a>


#### ANRUS_TOUCH_MODIFICATION_ACTIVE

<a id="ANRUS_PRIORITY_AUDIO_ACTIVE"></a>
<a id="anrus_priority_audio_active"></a>


#### ANRUS_PRIORITY_AUDIO_ACTIVE

<a id="ANRUS_PRIORITY_AUDIO_ACTIVE_NODUCK"></a>
<a id="anrus_priority_audio_active_noduck"></a>


#### ANRUS_PRIORITY_AUDIO_ACTIVE_NODUCK


### -param dwUtilityState [in]

Type: <b>DWORD</b>


The new settings for the system values indicated by <i>dwUtilityStateMask</i>. This parameter can be zero to reset the system values, or a combination of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ANRUS_ON_SCREEN_KEYBOARD_ACTIVE"></a><a id="anrus_on_screen_keyboard_active"></a><dl>
<dt><b>ANRUS_ON_SCREEN_KEYBOARD_ACTIVE</b></dt>
<dt>0x0000001</dt>
</dl>
</td>
<td width="60%">
The AT application is providing an on-screen keyboard.

</td>
</tr>
<tr>
<td width="40%"><a id="ANRUS_TOUCH_MODIFICATION_ACTIVE"></a><a id="anrus_touch_modification_active"></a><dl>
<dt><b>ANRUS_TOUCH_MODIFICATION_ACTIVE</b></dt>
<dt>0x0000002</dt>
</dl>
</td>
<td width="60%">
The AT application is consuming redirected touch input. 

</td>
</tr>
<tr>
<td width="40%"><a id="ANRUS_PRIORITY_AUDIO_ACTIVE"></a><a id="anrus_priority_audio_active"></a><dl>
<dt><b>ANRUS_PRIORITY_AUDIO_ACTIVE</b></dt>
<dt>0x0000004</dt>
</dl>
</td>
<td width="60%">
The AT application is relying on audio (such as text-to-speech) to convey essential information to the user and should remain audible over other system sounds.

</td>
</tr>
<tr>
<td width="40%"><a id="ANRUS_PRIORITY_AUDIO_ACTIVE_NODUCK"></a><a id="anrus_priority_audio_active_noduck"></a><dl>
<dt><b>ANRUS_PRIORITY_AUDIO_ACTIVE_NODUCK</b></dt>
<dt>0x0000008</dt>
</dl>
</td>
<td width="60%">
The AT application is relying on audio (such as text-to-speech) to convey essential information to the user but should not change relative to other system sounds.

</td>
</tr>
</table>
 


## -returns



Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns a standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.




## -remarks



Before it exits, an AT application should reset any system values that it previously set. 

This function requires the calling process to have UIAccess or higher privileges.  If the caller does not have the required privileges, the call to <b>AccSetRunningUtilityState</b> fails and returns <b>E_ACCESSDENIED</b>. For more information, see <a href="https://msdn.microsoft.com/0c3689e1-2124-4142-b0bd-233e95ee1285">Security Considerations for Assistive Technologies</a> and <a href="https://go.microsoft.com/fwlink/p/?linkid=207612">/MANIFESTUAC (Embeds UAC information in manifest)</a>.


#### Examples

This code example shows how to call the <b>AccSetRunningUtilityState</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (SUCCEEDED(hr))
{
    // Tell the system that an AT application has registered with the 
    // touch redirector.
    hr = AccSetRunningUtilityState(hwndTouchWindow, 
            ANRUS_TOUCH_MODIFICATION_ACTIVE, 
            ANRUS_TOUCH_MODIFICATION_ACTIVE);
    if (FAILED(hr))
    {
        MyErrorHandler(hr); // Application-defined error handler
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/0c3689e1-2124-4142-b0bd-233e95ee1285">Security Considerations for Assistive Technologies</a>
 

 


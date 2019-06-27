---
UID: NN:tapi3if.ITAutomatedPhoneControl
title: ITAutomatedPhoneControl (tapi3if.h)
author: windows-sdk-content
description: The ITAutomatedPhoneControl is a fully OLE automatable and scriptable interface exposed by the TAPI phone object.
old-location: tapi3\itautomatedphonecontrol.htm
tech.root: Tapi
ms.assetid: 60d4f079-75ee-4aeb-9e7c-0b16d90da754
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl, ITAutomatedPhoneControl interface [TAPI 2.2], ITAutomatedPhoneControl interface [TAPI 2.2],described, _tapi3_itautomatedphonecontrol, tapi3.itautomatedphonecontrol, tapi3if/ITAutomatedPhoneControl
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITAutomatedPhoneControl"
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAutomatedPhoneControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAutomatedPhoneControl interface


## -description


The 
<b>ITAutomatedPhoneControl</b> is a fully OLE automatable and scriptable interface exposed by the TAPI phone object. When a phone device is opened with owner privilege, you can call the 
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface to obtain an 
<b>ITAutomatedPhoneControl</b> interface pointer.

This interface performs several high-level phone-related functions:
<ul>
<li>Enable and configure automated control of the phone's tones and rings based on input from the phone's hookswitch and buttons.</li>
<li>Enable and configure automated call handling based on the phone's hookswitch state. For example, when the phone goes onhook while it is handling a connected call, the phone object can automatically invoke 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">ITBasicCallControl::Disconnect</a> on that call.</li>
<li>Generate specific tones on the audio devices associated with the phone, without accessing any audio APIs directly. The tone control allows an application to play tones on the audio devices associated with the phone, outside of the context of a call. Because these tones are not transmitted on any call, they are independent of the audio streaming functionality accessed through terminals.</li>
<li>Ring the phone without requiring information on whether the phone has a ringer and, if the phone has a ringer, determine the types of rings the phone supports.</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAutomatedPhoneControl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAutomatedPhoneControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAutomatedPhoneControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-enumerateselectedcalls">EnumerateSelectedCalls</a>
</td>
<td align="left" width="63%">
Gets an enumerator object indicating which calls are currently selected on this phone. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autodialtone">get_AutoDialtone</a>
</td>
<td align="left" width="63%">
Gets the automatic dial tone status for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autoendofnumbertimeout">get_AutoEndOfNumberTimeout</a>
</td>
<td align="left" width="63%">
Gets the current value of the <b>AutoEndOfNumberTimeout</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autokeypadtones">get_AutoKeypadTones</a>
</td>
<td align="left" width="63%">
Gets automatic phone keypad feedback tone generation status for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autokeypadtonesminimumduration">get_AutoKeypadTonesMinimumDuration</a>
</td>
<td align="left" width="63%">
Gets how long keypad tones play on PBS_DOWN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autostopringonoffhook">get_AutoStopRingOnOffHook</a>
</td>
<td align="left" width="63%">
Gets the current value of the <i>AutoStopRingOnOffHook</i> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autostoptonesononhook">get_AutoStopTonesOnOnHook</a>
</td>
<td align="left" width="63%">
Gets the automatic tone termination status for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autovolumecontrol">get_AutoVolumeControl</a>
</td>
<td align="left" width="63%">
Gets the current value of the <b>AutoVolumeControl</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autovolumecontrolrepeatdelay">get_AutoVolumeControlRepeatDelay</a>
</td>
<td align="left" width="63%">
Gets the delay, in milliseconds, before a volume button starts repeating when it is held down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autovolumecontrolrepeatperiod">get_AutoVolumeControlRepeatPeriod</a>
</td>
<td align="left" width="63%">
Gets the current value of the <b>AutoVolumeControlRepeatDelay</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_autovolumecontrolstep">get_AutoVolumeControlStep</a>
</td>
<td align="left" width="63%">
Gets the amount that the phone volume is adjusted when the volume button is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_phonehandlingenabled">get_PhoneHandlingEnabled</a>
</td>
<td align="left" width="63%">
Gets the current value of the <b>PhoneHandlingEnabled</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_ringer">get_Ringer</a>
</td>
<td align="left" width="63%">
Gets whether the phone is currently ringing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_selectedcalls">get_SelectedCalls</a>
</td>
<td align="left" width="63%">
Gets a VARIANT containing a pointer to a collection object indicating which calls are currently selected on this phone. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-get_tone">get_Tone</a>
</td>
<td align="left" width="63%">
Gets the type of tone, if any, currently being played.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autodialtone">put_AutoDialtone</a>
</td>
<td align="left" width="63%">
Enables or disables automatic dial tone response for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autoendofnumbertimeout">put_AutoEndOfNumberTimeout</a>
</td>
<td align="left" width="63%">
Sets the current value of the <b>AutoEndOfNumberTimeout</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtones">put_AutoKeypadTones</a>
</td>
<td align="left" width="63%">
Enables or disables automatic phone keypad feedback tone generation for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autokeypadtonesminimumduration">put_AutoKeypadTonesMinimumDuration</a>
</td>
<td align="left" width="63%">
Sets how long keypad tones play on PBS_DOWN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autostopringonoffhook">put_AutoStopRingOnOffHook</a>
</td>
<td align="left" width="63%">
Sets the current value of the <b>AutoStopRingOnOffHook</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autostoptonesononhook">put_AutoStopTonesOnOnHook</a>
</td>
<td align="left" width="63%">
Enables or disables automatic tone termination for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autovolumecontrol">put_AutoVolumeControl</a>
</td>
<td align="left" width="63%">
Enables or disables automatic phone volume control for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autovolumecontrolrepeatdelay">put_AutoVolumeControlRepeatDelay</a>
</td>
<td align="left" width="63%">
Sets the delay, in milliseconds, before a volume button starts repeating when it is held down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autovolumecontrolrepeatperiod">put_AutoVolumeControlRepeatPeriod</a>
</td>
<td align="left" width="63%">
Sets the period, in milliseconds, of button repeats when a volume button is held down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_autovolumecontrolstep">put_AutoVolumeControlStep</a>
</td>
<td align="left" width="63%">
Sets the amount that the phone volume is adjusted when the volume button is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-put_phonehandlingenabled">put_PhoneHandlingEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables all automatic phone interaction features for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-selectcall">SelectCall</a>
</td>
<td align="left" width="63%">
Selects the current phone onto a call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-startringer">StartRinger</a>
</td>
<td align="left" width="63%">
Starts the phone's ringer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-starttone">StartTone</a>
</td>
<td align="left" width="63%">
Outputs tones.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stopringer">StopRinger</a>
</td>
<td align="left" width="63%">
Stops the phone's ringer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stoptone">StopTone</a>
</td>
<td align="left" width="63%">
Stops any tone that is currently being played.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-unselectcall">UnselectCall</a>
</td>
<td align="left" width="63%">
Removes the phone from the call.

</td>
</tr>
</table> 


## -remarks



An 
<b>ITAutomatedPhoneControl</b> pointer becomes invalid when the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-close">ITPhone::Close</a> method is called.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>
 

 


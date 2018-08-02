---
UID: NN:tapi3if.ITAutomatedPhoneControl
title: ITAutomatedPhoneControl
author: windows-sdk-content
description: The ITAutomatedPhoneControl is a fully OLE automatable and scriptable interface exposed by the TAPI phone object.
old-location: tapi3\itautomatedphonecontrol.htm
old-project: Tapi
ms.assetid: 60d4f079-75ee-4aeb-9e7c-0b16d90da754
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITAutomatedPhoneControl, ITAutomatedPhoneControl interface [TAPI 2.2], ITAutomatedPhoneControl interface [TAPI 2.2],described, _tapi3_itautomatedphonecontrol, tapi3.itautomatedphonecontrol, tapi3if/ITAutomatedPhoneControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TERMINAL_TYPE
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAutomatedPhoneControl interface


## -description


The 
<b>ITAutomatedPhoneControl</b> is a fully OLE automatable and scriptable interface exposed by the TAPI phone object. When a phone device is opened with owner privilege, you can call the 
<a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method on the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface to obtain an 
<b>ITAutomatedPhoneControl</b> interface pointer.

This interface performs several high-level phone-related functions:
<ul>
<li>Enable and configure automated control of the phone's tones and rings based on input from the phone's hookswitch and buttons.</li>
<li>Enable and configure automated call handling based on the phone's hookswitch state. For example, when the phone goes onhook while it is handling a connected call, the phone object can automatically invoke 
<a href="https://msdn.microsoft.com/b7d556fd-d3f5-4b93-96a9-cc5c58fb8a95">ITBasicCallControl::Disconnect</a> on that call.</li>
<li>Generate specific tones on the audio devices associated with the phone, without accessing any audio APIs directly. The tone control allows an application to play tones on the audio devices associated with the phone, outside of the context of a call. Because these tones are not transmitted on any call, they are independent of the audio streaming functionality accessed through terminals.</li>
<li>Ring the phone without requiring information on whether the phone has a ringer and, if the phone has a ringer, determine the types of rings the phone supports.</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAutomatedPhoneControl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITAutomatedPhoneControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/534d453c-f47c-48e1-af59-bfa452e2d8d8">EnumerateSelectedCalls</a>
</td>
<td align="left" width="63%">
Gets an enumerator object indicating which calls are currently selected on this phone. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/977be70d-bb2d-490a-afd1-8e7f496b10ae">get_AutoDialtone</a>
</td>
<td align="left" width="63%">
Gets the automatic dial tone status for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5bc3176-7237-4c20-808a-b2d028ae4344">get_AutoEndOfNumberTimeout</a>
</td>
<td align="left" width="63%">
Gets the current value of the <b>AutoEndOfNumberTimeout</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd6c2b1c-53c5-40f9-bb5e-51c48d5bc944">get_AutoKeypadTones</a>
</td>
<td align="left" width="63%">
Gets automatic phone keypad feedback tone generation status for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f1ae3f0-ae6a-408a-ac53-e4181ecf2c4b">get_AutoKeypadTonesMinimumDuration</a>
</td>
<td align="left" width="63%">
Gets how long keypad tones play on PBS_DOWN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/357266e7-b103-43c1-a6af-b00347c90f51">get_AutoStopRingOnOffHook</a>
</td>
<td align="left" width="63%">
Gets the current value of the <i>AutoStopRingOnOffHook</i> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ece8d7a-b280-42b6-9f51-d88650488699">get_AutoStopTonesOnOnHook</a>
</td>
<td align="left" width="63%">
Gets the automatic tone termination status for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dae6d41-59d8-40ab-901f-91d97b59ac83">get_AutoVolumeControl</a>
</td>
<td align="left" width="63%">
Gets the current value of the <b>AutoVolumeControl</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a26fd436-b792-4415-bc47-eca2b1114002">get_AutoVolumeControlRepeatDelay</a>
</td>
<td align="left" width="63%">
Gets the delay, in milliseconds, before a volume button starts repeating when it is held down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ab52127-62e2-4e80-980a-8b29b51fa91f">get_AutoVolumeControlRepeatPeriod</a>
</td>
<td align="left" width="63%">
Gets the current value of the <b>AutoVolumeControlRepeatDelay</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cf6beba-36ca-417b-91b4-9c008a14efef">get_AutoVolumeControlStep</a>
</td>
<td align="left" width="63%">
Gets the amount that the phone volume is adjusted when the volume button is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6174caa-6045-4b82-9b13-11b86f8cf8a8">get_PhoneHandlingEnabled</a>
</td>
<td align="left" width="63%">
Gets the current value of the <b>PhoneHandlingEnabled</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc4daec0-7f55-4c76-b8a0-19307c7046dc">get_Ringer</a>
</td>
<td align="left" width="63%">
Gets whether the phone is currently ringing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50196789-c243-4279-8748-960898323992">get_SelectedCalls</a>
</td>
<td align="left" width="63%">
Gets a VARIANT containing a pointer to a collection object indicating which calls are currently selected on this phone. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62e7ae4d-7839-4568-b8b2-7a377601ea7c">get_Tone</a>
</td>
<td align="left" width="63%">
Gets the type of tone, if any, currently being played.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a906104f-01eb-4c53-9571-7068a98d48a5">put_AutoDialtone</a>
</td>
<td align="left" width="63%">
Enables or disables automatic dial tone response for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/985466a4-212b-48fd-b901-5fd3cc37eb0e">put_AutoEndOfNumberTimeout</a>
</td>
<td align="left" width="63%">
Sets the current value of the <b>AutoEndOfNumberTimeout</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a57c0ef-440a-4939-8d15-edb0c59dc1a4">put_AutoKeypadTones</a>
</td>
<td align="left" width="63%">
Enables or disables automatic phone keypad feedback tone generation for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c4bdd45-7d19-47a4-aa18-5944d3e58797">put_AutoKeypadTonesMinimumDuration</a>
</td>
<td align="left" width="63%">
Sets how long keypad tones play on PBS_DOWN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/114e17e2-63e7-47f9-8ae7-1c7e452376f6">put_AutoStopRingOnOffHook</a>
</td>
<td align="left" width="63%">
Sets the current value of the <b>AutoStopRingOnOffHook</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0047b631-91fc-47fb-aa38-cedb096a5646">put_AutoStopTonesOnOnHook</a>
</td>
<td align="left" width="63%">
Enables or disables automatic tone termination for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d45ef58-a7d7-41ab-b06a-9d53bf79690a">put_AutoVolumeControl</a>
</td>
<td align="left" width="63%">
Enables or disables automatic phone volume control for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a00993af-2ff2-4f91-889e-b0d3ae550642">put_AutoVolumeControlRepeatDelay</a>
</td>
<td align="left" width="63%">
Sets the delay, in milliseconds, before a volume button starts repeating when it is held down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/932b1092-6396-4ee9-84d7-1e28b09d132f">put_AutoVolumeControlRepeatPeriod</a>
</td>
<td align="left" width="63%">
Sets the period, in milliseconds, of button repeats when a volume button is held down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19766507-7a15-4c45-91bd-4b49ceb177e6">put_AutoVolumeControlStep</a>
</td>
<td align="left" width="63%">
Sets the amount that the phone volume is adjusted when the volume button is pressed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6759b811-2fc1-4827-a03e-d19335520829">put_PhoneHandlingEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables all automatic phone interaction features for this phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9e721cb-8f62-420d-bfc1-f8e634f0f2d4">SelectCall</a>
</td>
<td align="left" width="63%">
Selects the current phone onto a call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf94aab7-6b12-43f8-b49f-a7cf6617dd57">StartRinger</a>
</td>
<td align="left" width="63%">
Starts the phone's ringer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04cce8d6-ccab-4eeb-a97c-3bc24ec3fc00">StartTone</a>
</td>
<td align="left" width="63%">
Outputs tones.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74829b2a-6530-40d2-8693-7c6104de7309">StopRinger</a>
</td>
<td align="left" width="63%">
Stops the phone's ringer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/618743c3-6d4a-4cab-a4fc-7cd4e3b8cdd9">StopTone</a>
</td>
<td align="left" width="63%">
Stops any tone that is currently being played.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c2a9899-add7-4c09-b32e-11061fc2c5a5">UnselectCall</a>
</td>
<td align="left" width="63%">
Removes the phone from the call.

</td>
</tr>
</table> 


## -remarks



An 
<b>ITAutomatedPhoneControl</b> pointer becomes invalid when the 
<a href="https://msdn.microsoft.com/1eae1a14-dd5e-4ba9-8e6e-71e9956cb3e3">ITPhone::Close</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>
 

 


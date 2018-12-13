---
UID: NN:tapi3if.ITPhone
title: ITPhone
author: windows-sdk-content
description: The ITPhone interface is the main interface for the new Phone objects in the TAPI 3.1 object model.
old-location: tapi3\itphone.htm
tech.root: tapi
ms.assetid: 94dff33c-67a1-4df8-9ef5-2b6524438f6f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITPhone, ITPhone interface [TAPI 2.2], ITPhone interface [TAPI 2.2],described, _tapi3_itphone, tapi3.itphone, tapi3if/ITPhone
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITPhone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone interface


## -description


The 
<b>ITPhone</b> interface is the main interface for the new Phone objects in the TAPI 3.1 object model. This interface allows access to the phone device at a level comparable to that available with the TAPI 2.<i>x</i> C API. The interface also allows the application to determine which addresses the phone is usable on, and to get a list of terminals associated with the phone. The 
<a href="https://msdn.microsoft.com/7ea1e851-00df-4b32-ba37-c562da983102">IEnumPhone::Next</a> and <a href="https://msdn.microsoft.com/81b61c98-839a-488b-a0da-085f8891197c">ITPhoneEvent::get_Phone</a> methods create the 
<b>ITPhone</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPhone</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITPhone</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPhone</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1eae1a14-dd5e-4ba9-8e6e-71e9956cb3e3">Close</a>
</td>
<td align="left" width="63%">
Closes the phone device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fba4bf7e-8c9d-4d34-ac56-aa47dff6f57c">DeviceSpecific</a>
</td>
<td align="left" width="63%">
Provides access to device-specific features. For C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/828d34e5-efac-4776-85a2-51eb94d68dac">DeviceSpecificVariant</a>
</td>
<td align="left" width="63%">
Provides access to device-specific features. For Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d72f6877-eb89-400e-a1bc-393116a9666f">EnumerateAddresses</a>
</td>
<td align="left" width="63%">
Enumerates the addresses on which the phone can be used. For C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bb15dc1-c1f0-4da5-8217-baedb45b70f7">EnumeratePreferredAddresses</a>
</td>
<td align="left" width="63%">
Enumerates addresses that the phone is preferred for use on. For C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87c756e3-abd0-4dff-b815-ff7dd60902f7">EnumerateTerminals</a>
</td>
<td align="left" width="63%">
Gets an enumeration of terminals that are associated with the phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/823db8d1-e4e3-4cfb-a864-5ad57a44ebc6">get_Addresses</a>
</td>
<td align="left" width="63%">
Gets the collection of addresses on which the phone can be used. For Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a884c0b4-141a-4f04-8cfb-7ae6b1ec11b3">get_ButtonFunction</a>
</td>
<td align="left" width="63%">
Gets the button function associated with a particular button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b3173bf-1c79-4c5d-a2bc-3b3ae4f0ae8a">get_ButtonMode</a>
</td>
<td align="left" width="63%">
Gets the button mode associated with a particular button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f14e0593-0f03-4119-b80a-12d32b68aa99">get_ButtonState</a>
</td>
<td align="left" width="63%">
Gets the button state associated with a particular button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75a216fb-7bb3-4178-baa5-8ba478bd5422">get_ButtonText</a>
</td>
<td align="left" width="63%">
Gets the button text associated with a particular button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/259982d7-8c28-4c0d-81b3-e4ec49fc9765">get_Display</a>
</td>
<td align="left" width="63%">
Gets the display for the phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4560b447-45af-482a-b97b-dd0cbdb52466">get_HookSwitchState</a>
</td>
<td align="left" width="63%">
Gets the current hookswitch state for a particular hookswitch device on the phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e0fa135-304a-4598-a6cd-2e5734b3678c">get_LampMode</a>
</td>
<td align="left" width="63%">
Gets the current lamp mode for the given lamp.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9397aa8-2be4-4775-8123-975bdd58a6b5">get_PhoneCapsBuffer</a>
</td>
<td align="left" width="63%">
Gets a buffer capability/information about the phone, based on the 
<a href="https://msdn.microsoft.com/208efd60-58b2-4d0a-b757-29b1db017195">PHONECAPS_BUFFER</a> enum passed in. For Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d7804a7-616b-4efc-9f3b-6d7b1fda1bf6">get_PhoneCapsLong</a>
</td>
<td align="left" width="63%">
Gets a capability of the phone, based on the 
<a href="https://msdn.microsoft.com/7a73d5ff-d08a-46e6-b4ad-4f3b973967a7">PHONECAPS_LONG</a> enum passed in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4a0ed77-455e-428c-a3e5-cd467e47b5b2">get_PhoneCapsString</a>
</td>
<td align="left" width="63%">
Gets a string capability/information about the phone, based on the 
<a href="https://msdn.microsoft.com/3ff60aa8-9a77-48a1-a60f-1e1d31653728">PHONECAPS_STRING</a> enum passed in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bda43c65-a1f9-4143-b808-2a4e61220b1b">get_PreferredAddresses</a>
</td>
<td align="left" width="63%">
Returns a collection of addresses that the phone is preferred for use on. For Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88103a48-a5cd-43a7-a88e-9b16313b35c2">get_Privilege</a>
</td>
<td align="left" width="63%">
Gets the privilege of the open phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55f6a75c-dffb-46e7-8679-70c7d59ff5b4">get_RingMode</a>
</td>
<td align="left" width="63%">
Gets the phone's ring mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/147553f1-74a7-4f80-bbf3-b140d9b375ba">get_RingVolume</a>
</td>
<td align="left" width="63%">
Gets the phone's volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09e5921c-c7da-40fc-902a-1e22ebe19b0a">get_Terminals</a>
</td>
<td align="left" width="63%">
Gets a collection of terminals that are associated with the phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/239902ca-0e9e-4b8d-927d-ee46a35dd9d8">GetPhoneCapsBuffer</a>
</td>
<td align="left" width="63%">
Gets a buffer capability/information about the phone, based on the 
<a href="https://msdn.microsoft.com/208efd60-58b2-4d0a-b757-29b1db017195">PHONECAPS_BUFFER</a> enum passed in. For C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a29311bf-0fe4-4e58-96cc-2e3734c32aee">NegotiateExtVersion</a>
</td>
<td align="left" width="63%">
Negotiates an extension version to use with the specified phone device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">Open</a>
</td>
<td align="left" width="63%">
Opens the phone device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8002ab8a-a15d-4a1f-b0c3-7a15c61cb6c4">put_ButtonFunction</a>
</td>
<td align="left" width="63%">
Puts the button function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2287c86-5884-4890-956c-fcc26c426cd3">put_ButtonMode</a>
</td>
<td align="left" width="63%">
Sets the button mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b50427e9-94cd-47bb-910f-2f879df9bcf8">put_ButtonText</a>
</td>
<td align="left" width="63%">
Sets the button text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab0bcd30-6985-4f53-a39d-90230421b6f4">put_HookSwitchState</a>
</td>
<td align="left" width="63%">
Sets the current hookswitch state for a particular hookswitch device on the phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0445cf2c-1b00-4136-bdab-3c6e0669ef11">put_LampMode</a>
</td>
<td align="left" width="63%">
Sets the current lamp mode for the given lamp.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f693bf24-540d-4509-bf0c-01be27f823f8">put_RingMode</a>
</td>
<td align="left" width="63%">
Sets the phone's ring mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/858ca6a8-a53b-4858-b4b0-985230ec8ea0">put_RingVolume</a>
</td>
<td align="left" width="63%">
Sets the phone's volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/690756c4-201d-472d-b536-452074226701">SetDisplay</a>
</td>
<td align="left" width="63%">
Sets the display for the phone.

</td>
</tr>
</table> 


---
UID: NN:tapi3if.ITPhone
title: ITPhone (tapi3if.h)
description: The ITPhone interface is the main interface for the new Phone objects in the TAPI 3.1 object model.
old-location: tapi3\itphone.htm
tech.root: Tapi
ms.assetid: 94dff33c-67a1-4df8-9ef5-2b6524438f6f
ms.date: 12/05/2018
ms.keywords: ITPhone, ITPhone interface [TAPI 2.2], ITPhone interface [TAPI 2.2],described, _tapi3_itphone, tapi3.itphone, tapi3if/ITPhone
f1_keywords:
- tapi3if/ITPhone
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhone interface


## -description


The 
<b>ITPhone</b> interface is the main interface for the new Phone objects in the TAPI 3.1 object model. This interface allows access to the phone device at a level comparable to that available with the TAPI 2.<i>x</i> C API. The interface also allows the application to determine which addresses the phone is usable on, and to get a list of terminals associated with the phone. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumphone-next">IEnumPhone::Next</a> and <a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_phone">ITPhoneEvent::get_Phone</a> methods create the 
<b>ITPhone</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPhone</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPhone</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-close">Close</a>
</td>
<td align="left" width="63%">
Closes the phone device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-devicespecific">DeviceSpecific</a>
</td>
<td align="left" width="63%">
Provides access to device-specific features. For C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-devicespecificvariant">DeviceSpecificVariant</a>
</td>
<td align="left" width="63%">
Provides access to device-specific features. For Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-enumerateaddresses">EnumerateAddresses</a>
</td>
<td align="left" width="63%">
Enumerates the addresses on which the phone can be used. For C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-enumeratepreferredaddresses">EnumeratePreferredAddresses</a>
</td>
<td align="left" width="63%">
Enumerates addresses that the phone is preferred for use on. For C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-enumerateterminals">EnumerateTerminals</a>
</td>
<td align="left" width="63%">
Gets an enumeration of terminals that are associated with the phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_addresses">get_Addresses</a>
</td>
<td align="left" width="63%">
Gets the collection of addresses on which the phone can be used. For Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttonfunction">get_ButtonFunction</a>
</td>
<td align="left" width="63%">
Gets the button function associated with a particular button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttonmode">get_ButtonMode</a>
</td>
<td align="left" width="63%">
Gets the button mode associated with a particular button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttonstate">get_ButtonState</a>
</td>
<td align="left" width="63%">
Gets the button state associated with a particular button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_buttontext">get_ButtonText</a>
</td>
<td align="left" width="63%">
Gets the button text associated with a particular button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_display">get_Display</a>
</td>
<td align="left" width="63%">
Gets the display for the phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_hookswitchstate">get_HookSwitchState</a>
</td>
<td align="left" width="63%">
Gets the current hookswitch state for a particular hookswitch device on the phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_lampmode">get_LampMode</a>
</td>
<td align="left" width="63%">
Gets the current lamp mode for the given lamp.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_phonecapsbuffer">get_PhoneCapsBuffer</a>
</td>
<td align="left" width="63%">
Gets a buffer capability/information about the phone, based on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_buffer">PHONECAPS_BUFFER</a> enum passed in. For Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_phonecapslong">get_PhoneCapsLong</a>
</td>
<td align="left" width="63%">
Gets a capability of the phone, based on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_long">PHONECAPS_LONG</a> enum passed in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_phonecapsstring">get_PhoneCapsString</a>
</td>
<td align="left" width="63%">
Gets a string capability/information about the phone, based on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_string">PHONECAPS_STRING</a> enum passed in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_preferredaddresses">get_PreferredAddresses</a>
</td>
<td align="left" width="63%">
Returns a collection of addresses that the phone is preferred for use on. For Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_privilege">get_Privilege</a>
</td>
<td align="left" width="63%">
Gets the privilege of the open phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_ringmode">get_RingMode</a>
</td>
<td align="left" width="63%">
Gets the phone's ring mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_ringvolume">get_RingVolume</a>
</td>
<td align="left" width="63%">
Gets the phone's volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_terminals">get_Terminals</a>
</td>
<td align="left" width="63%">
Gets a collection of terminals that are associated with the phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-getphonecapsbuffer">GetPhoneCapsBuffer</a>
</td>
<td align="left" width="63%">
Gets a buffer capability/information about the phone, based on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phonecaps_buffer">PHONECAPS_BUFFER</a> enum passed in. For C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-negotiateextversion">NegotiateExtVersion</a>
</td>
<td align="left" width="63%">
Negotiates an extension version to use with the specified phone device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">Open</a>
</td>
<td align="left" width="63%">
Opens the phone device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_buttonfunction">put_ButtonFunction</a>
</td>
<td align="left" width="63%">
Puts the button function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_buttonmode">put_ButtonMode</a>
</td>
<td align="left" width="63%">
Sets the button mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_buttontext">put_ButtonText</a>
</td>
<td align="left" width="63%">
Sets the button text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_hookswitchstate">put_HookSwitchState</a>
</td>
<td align="left" width="63%">
Sets the current hookswitch state for a particular hookswitch device on the phone.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_lampmode">put_LampMode</a>
</td>
<td align="left" width="63%">
Sets the current lamp mode for the given lamp.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_ringmode">put_RingMode</a>
</td>
<td align="left" width="63%">
Sets the phone's ring mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_ringvolume">put_RingVolume</a>
</td>
<td align="left" width="63%">
Sets the phone's volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphone-setdisplay">SetDisplay</a>
</td>
<td align="left" width="63%">
Sets the display for the phone.

</td>
</tr>
</table> 


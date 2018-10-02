---
UID: NS:raseapif._PPP_EAP_OUTPUT
title: "_PPP_EAP_OUTPUT"
author: windows-sdk-content
description: The authentication protocol uses the PPP_EAP_OUTPUT structure to communicate requests and status information to the Connection Manager on return from calls to RasEapMakeMessage.
old-location: eap\ppp_eap_output.htm
tech.root: EAP
ms.assetid: d1634973-f6af-4be3-914a-513098c5fccf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PPPP_EAP_OUTPUT, PPPP_EAP_OUTPUT, PPPP_EAP_OUTPUT structure pointer [EAP], PPP_EAP_OUTPUT, PPP_EAP_OUTPUT structure [EAP], _PPP_EAP_OUTPUT, _eap_ppp_eap_output, eap.ppp_eap_output, raseapif/PPPP_EAP_OUTPUT, raseapif/PPP_EAP_OUTPUT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: raseapif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Raseapif.h
api_name:
 - PPP_EAP_OUTPUT
product: Windows
targetos: Windows
req.typenames: PPP_EAP_OUTPUT, *PPPP_EAP_OUTPUT
req.redist: 
---

# _PPP_EAP_OUTPUT structure


## -description


The authentication protocol uses the 
<b>PPP_EAP_OUTPUT</b> structure to communicate requests and status information to the Connection Manager on return from calls to 
<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>.


## -struct-fields




### -field dwSizeInBytes

Specifies the size of this structure.


### -field Action

Specifies a 
<a href="https://msdn.microsoft.com/5b1ead41-1fc0-41af-8614-3246d220c88d">PPP_EAP_ACTION</a> value. The Connection Manager carries out this action on behalf of the authentication protocol.


### -field dwAuthResultCode

Specifies whether authentication was successful. Any nonzero value for <b>dwAuthResultCode</b> indicates failure. The failure code must come from Winerror.h, Raserror.h or Mprerror.h. This member is valid only if the <b>Action</b> member has a value of <b>EAPACTION_Done</b> or <b>EAPACTION_SendAndDone</b>.


### -field pUserAttributes

Pointer to an optional array of 
<a href="https://msdn.microsoft.com/36659154-de2b-4a94-b25e-b731a4ef9d99">RAS_AUTH_ATTRIBUTE</a> structures. The array is terminated by a structure with an <b>raaType</b> member that has a value of <b>raatMinimum</b> (see 
<a href="https://msdn.microsoft.com/0cb99318-2874-4945-ae32-cb5d90be9dee">RAS_AUTH_ATTRIBUTE_TYPE</a>). 




This member should be set on the authenticator side when <b>Action</b> is <b>EAPACTION_Authenticate</b>, or when <b>Action</b> is <b>EAPACTION_Done</b> or <b>EAPACTION_SendAndDone</b> and <b>dwAuthResultCode</b> is zero.

When <b>Action</b> is <b>EAPACTION_Authenticate</b>, the array may contain additional attributes necessary to authenticate the user, e.g. the user-password. If the authentication protocol passes in only the user name, RAS does not invoke the authentication provider to authenticate the user, Instead, RAS just passes back the current attributes for the user.

When <b>Action</b> is <b>EAPACTION_Done</b> or <b>EAPACTION_SendAndDone</b>, and <b>dwAuthResultCode</b> is zero, the array may contain additional attributes to assign to the user. These attributes overwrite any attributes of the same type returned by the authentication provider.

The authentication protocol frees this memory in its 
<a href="https://msdn.microsoft.com/52204bc6-03ed-4e8c-819f-b54174ccdbd4">RasEapEnd</a> function.


### -field fInvokeInteractiveUI

Specifies whether RAS should invoke the authentication protocol's interactive UI. If the authentication protocol sets this member to <b>TRUE</b>, RAS invokes the interactive UI, by calling the 
<a href="https://msdn.microsoft.com/71dd40c9-acbd-4fb6-800d-d3f83a61b7b8">RasEapInvokeInteractiveUI</a> function provided by the authentication protocol.


### -field pUIContextData

Pointer to context data that RAS should pass in the call to 
<a href="https://msdn.microsoft.com/71dd40c9-acbd-4fb6-800d-d3f83a61b7b8">RasEapInvokeInteractiveUI</a>. The authentication protocol should free this memory in its implementation of 
<a href="https://msdn.microsoft.com/52204bc6-03ed-4e8c-819f-b54174ccdbd4">RasEapEnd</a>.


### -field dwSizeOfUIContextData

Specifies the size of the context data that RAS should pass in the call to 
<a href="https://msdn.microsoft.com/71dd40c9-acbd-4fb6-800d-d3f83a61b7b8">RasEapInvokeInteractiveUI</a>.


### -field fSaveConnectionData

Specifies whether RAS should save the information pointed to by the <b>pConnectionData</b> member. If <b>fSaveConnectionData</b> is <b>TRUE</b>, RAS will save the data in the phone book. Only valid for the process that is being authenticated.


### -field pConnectionData

Identifies data specific to the connection, that is, data not specific to any particular user. If the <b>fSaveConnectionData</b> member is <b>TRUE</b>, RAS saves the connection data in the phone book. The authentication protocol should free the memory occupied by this data during the call to 
<a href="https://msdn.microsoft.com/52204bc6-03ed-4e8c-819f-b54174ccdbd4">RasEapEnd</a>.


### -field dwSizeOfConnectionData

Specifies the size, in bytes, of the data pointed to by the <b>pConnectionData</b> member. 

					


### -field fSaveUserData

Specifies whether RAS should save the user data pointed to by the <b>pUserData</b> member. If this parameter is <b>TRUE</b>, RAS saves the user-specific data in the registry under <b>HKEY_CURRENT_USER</b>.


### -field pUserData

Pointer to user data that RAS should save in the registry. RAS saves this data in the registry under <b>HKEY_CURRENT_USER</b>. The authentication protocol should free this memory during the call to 
<a href="https://msdn.microsoft.com/52204bc6-03ed-4e8c-819f-b54174ccdbd4">RasEapEnd</a>.


### -field dwSizeOfUserData

Specifies the size in bytes of the data pointed to by <b>pUserData</b>.


### -field pNgcKerbTicket

 


### -field fSaveToCredMan

 




## -remarks



Use the 
<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a> function to pass the 
<b>PPP_EAP_OUTPUT</b> structure between the authentication protocol and the Connection Manager.

The authentication protocol can use the 
<b>PPP_EAP_OUTPUT</b> structure to return the Microsoft Point-to-Point Encryption (MPPE) session keys. The authentication protocol  must place the session keys in the value field of a sub-attribute contained within the value field of an attribute of type <b>raatVendorSpecific</b> (see 
<a href="https://msdn.microsoft.com/0cb99318-2874-4945-ae32-cb5d90be9dee">RAS_AUTH_ATTRIBUTE_TYPE</a>). The sub-attribute should have a Vendor-ID of 311 (Microsoft) and Vendor-Type of MS-MPPE-Recv-Keys (17) and MS-MPPE-Send-Keys (16). The authentication protocol must set the <b>pUserAttributes</b> member to point to the <b>raatVendorSpecific</b> attribute, and set the <b>Action</b> member to <b>EAPACTION_Done</b> or <b>EAPACTION_SendAndDone</b>. For more information about the format of the MPPE sub-attribute see 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84047">Microsoft Vendor-specific RADIUS Attributes</a>. For more information about attribute formats see 
<a href="https://msdn.microsoft.com/36659154-de2b-4a94-b25e-b731a4ef9d99">RAS_AUTH_ATTRIBUTE</a>, 
<a href="https://msdn.microsoft.com/0cb99318-2874-4945-ae32-cb5d90be9dee">RAS_AUTH_ATTRIBUTE_TYPE</a>, and 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a>.

<div class="alert"><b>Note</b>  When formatting attributes for encryption keys, it is strongly recommended that you  use MSCHAPv2 and its MS-MPPE-Recv-Keys and MS-MPPE-Send-Keys,  which create <i>strong encryption</i> rather than  MSCHAPv1 and its MS-CHAP-MPPE-Keys.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f2f1cf75-18d4-4764-a747-24662f166eb7">EAP Structures</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/5b1ead41-1fc0-41af-8614-3246d220c88d">PPP_EAP_ACTION</a>



<a href="https://msdn.microsoft.com/36659154-de2b-4a94-b25e-b731a4ef9d99">RAS_AUTH_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/71dd40c9-acbd-4fb6-800d-d3f83a61b7b8">RasEapInvokeInteractiveUI</a>



<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>
 

 


---
UID: NF:mdhcp.IMcastScope.get_InterfaceID
title: IMcastScope::get_InterfaceID (mdhcp.h)
description: The get_InterfaceID method obtains an interface identifier of this scope, which identifies the interface on which the server that published this scope resides. This is normally the network address of the interface.
helpviewer_keywords: ["IMcastScope interface [TAPI 2.2]","get_InterfaceID method","IMcastScope.get_InterfaceID","IMcastScope::get_InterfaceID","_tapi3_imcastscope_get_interfaceid","get_InterfaceID","get_InterfaceID method [TAPI 2.2]","get_InterfaceID method [TAPI 2.2]","IMcastScope interface","mdhcp/IMcastScope::get_InterfaceID","tapi3.imcastscope_get_interfaceid"]
old-location: tapi3\imcastscope_get_interfaceid.htm
tech.root: tapi3
ms.assetid: 376ccbe4-ad83-4eef-88bd-11ed95d14359
ms.date: 12/05/2018
ms.keywords: IMcastScope interface [TAPI 2.2],get_InterfaceID method, IMcastScope.get_InterfaceID, IMcastScope::get_InterfaceID, _tapi3_imcastscope_get_interfaceid, get_InterfaceID, get_InterfaceID method [TAPI 2.2], get_InterfaceID method [TAPI 2.2],IMcastScope interface, mdhcp/IMcastScope::get_InterfaceID, tapi3.imcastscope_get_interfaceid
req.header: mdhcp.h
req.include-header: 
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
req.dll: Mdhcp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMcastScope::get_InterfaceID
 - mdhcp/IMcastScope::get_InterfaceID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IMcastScope.get_InterfaceID
---

# IMcastScope::get_InterfaceID


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_InterfaceID</b> method obtains an interface identifier of this scope, which identifies the interface on which the server that published this scope resides. This is normally the network address of the interface.

## -parameters

### -param pID [out]

Pointer to a <b>LONG</b> that will receive the server ID of this scope, which is the ID that was assigned to the multicast address allocation server that published this scope at the time that the server was configured.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The caller passed in an invalid pointer argument.

</td>
</tr>
</table>

## -remarks

The InterfaceID is provided for informational purposes only; it is not required as input to any of the methods in these interfaces. However, it may factor into the application's (or the user's) decision as to which scope to use when requesting an address. This is because, in a multihomed scenario, using a multicast address on one network that was obtained from a server on another network may cause address conflicts.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a>
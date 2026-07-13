---
UID: NF:drt.DrtOpen
title: DrtOpen function (drt.h)
description: DrtOpen function creates a local Distributed Routing Table instance against criteria specified by the DRT_SETTINGS structure.
helpviewer_keywords: ["DrtOpen","DrtOpen function [Peer Networking]","drt/DrtOpen","p2p.drtopen"]
old-location: p2p\drtopen.htm
tech.root: p2p
ms.assetid: 67320767-f622-478a-a886-bbea1650ac1a
ms.date: 12/05/2018
ms.keywords: DrtOpen, DrtOpen function [Peer Networking], drt/DrtOpen, p2p.drtopen
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtOpen
 - drt/DrtOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtOpen
---

# DrtOpen function


## -description

The <b>DrtOpen</b> function creates a local Distributed Routing Table instance against criteria specified by the <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> structure.

## -parameters

### -param pSettings [in]

Pointer to the <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> structure which specifies the settings used for the creation of the DRT instance.

### -param hEvent [in]

Handle to the event signaled when an event occurs.

### -param pvContext [in, optional]

User defined context data which is passed  to the application via  events.

### -param phDrt [out]

The new handle associated with the DRT. This is used in all future operations on the DRT instance.

## -returns

This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>phDrt</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_SETTINGS</b></dt>
</dl>
</td>
<td width="60%">
<i>pSettings</i> is <b>NULL</b> or the <b>dwSize</b> member value of <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a>  is not equal to the size of the <b>DRT_SETTINGS</b> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_KEY_SIZE</b></dt>
</dl>
</td>
<td width="60%">
<i>cbKey</i> is not equal to 256 bits.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_MAX_ADDRESSES</b></dt>
</dl>
</td>
<td width="60%">
The <b>ulMaxRoutingAddresses</b> member of <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> specifies less than 1 or more than 20 as the maximum number of addresses.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_TRANSPORT_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
The <b>hTransport</b> member in <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> is <b>NULL</b> or some fields of the Transport are <b>NULL</b>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_SECURITY_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <b>eSecurityMode</b> member of <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> specifies  an invalid security mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_SECURITY_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
The <b>pSecurityProvider</b> member of <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_BOOTSTRAP_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
The  <b>pBootstrapProvider</b> member of <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> is <b>NULL</b> or some fields of the bootstrap provider are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_INSTANCE_PREFIX</b></dt>
</dl>
</td>
<td width="60%">
The size of the <b>pwzDrtInstancePrefix</b> specified in <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> is larger than the maximum prefix length (128).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system cannot allocate memory for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_BOOTSTRAPPROVIDER_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The bootstrap provider is already attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_SECURITYPROVIDER_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The security provider is already attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_TRANSPORTPROVIDER_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The transport provider is already attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_CERT_CHAIN</b></dt>
</dl>
</td>
<td width="60%">
The certification chain is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_CAPABILITY_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Local certificate cannot be <b>NULL</b> in DRT_SECURE_MEMBERSHIP and  DRT_SECURE_CONFIDENTIALPAYLOAD security.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_SHUTTING_DOWN</b></dt>
</dl>
</td>
<td width="60%">
Transport is shutting down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_ALREADY_BOUND</b></dt>
</dl>
</td>
<td width="60%">
Transport is already bound.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_S_RETRY</b></dt>
</dl>
</td>
<td width="60%">
Bootstrap provider failed to locate other nodes, but may be successful in a second attempt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
Transport provider parameter is <b>NULL</b> or invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORTPROVIDER_NOT_ATTACHED</b></dt>
</dl>
</td>
<td width="60%">
Transport is not attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unexpected fatal error occurred.

</td>
</tr>
</table>

## -remarks

 After <b>DrtOpen</b> is called, the DRT will begin the bootstrapping procedure and move to the <b>DRT_ACTIVE</b> or <b>DRT_ALONE</b> state, depending on the success of the bootstrap.

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a>



<a href="/windows/desktop/api/drt/nf-drt-drtclose">DrtClose</a>
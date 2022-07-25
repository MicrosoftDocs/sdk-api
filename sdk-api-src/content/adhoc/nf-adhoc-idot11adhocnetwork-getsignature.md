---
UID: NF:adhoc.IDot11AdHocNetwork.GetSignature
title: IDot11AdHocNetwork::GetSignature (adhoc.h)
description: Gets the unique signature associated with the ad hoc network.
helpviewer_keywords: ["GetSignature","GetSignature method [NativeWIFI]","GetSignature method [NativeWIFI]","IDot11AdHocNetwork interface","IDot11AdHocNetwork interface [NativeWIFI]","GetSignature method","IDot11AdHocNetwork.GetSignature","IDot11AdHocNetwork::GetSignature","adhoc/IDot11AdHocNetwork::GetSignature","nwifi.idot11adhocnetwork_getsignature"]
old-location: nwifi\idot11adhocnetwork_getsignature.htm
tech.root: nwifi
ms.assetid: 0a59a8bd-d2eb-48c6-8480-dc4dea335d22
ms.date: 12/05/2018
ms.keywords: GetSignature, GetSignature method [NativeWIFI], GetSignature method [NativeWIFI],IDot11AdHocNetwork interface, IDot11AdHocNetwork interface [NativeWIFI],GetSignature method, IDot11AdHocNetwork.GetSignature, IDot11AdHocNetwork::GetSignature, adhoc/IDot11AdHocNetwork::GetSignature, nwifi.idot11adhocnetwork_getsignature
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDot11AdHocNetwork::GetSignature
 - adhoc/IDot11AdHocNetwork::GetSignature
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocNetwork.GetSignature
---

# IDot11AdHocNetwork::GetSignature


## -description

Gets the unique signature associated with the ad hoc network. The signature uniquely identifies an <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a> object with a particular set of attributes.

## -parameters

### -param pSignature [in, out]

A signature that uniquely identifies an ad hoc network. This signature is generated  from certain network attributes.

## -returns

Possible return values include, but are not limited to, the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
</table>

## -remarks

Do not cache the returned signature locally. Whenever a network object changes, its signature changes.  Actions that are not associated with notifications, such as  saving the network's profile, can cause the signature to change.

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a>
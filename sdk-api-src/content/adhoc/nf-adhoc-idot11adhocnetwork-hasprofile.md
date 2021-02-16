---
UID: NF:adhoc.IDot11AdHocNetwork.HasProfile
title: IDot11AdHocNetwork::HasProfile (adhoc.h)
description: Returns a boolean value that specifies whether there is a saved profile associated with the network.
helpviewer_keywords: ["HasProfile","HasProfile method [NativeWIFI]","HasProfile method [NativeWIFI]","IDot11AdHocNetwork interface","IDot11AdHocNetwork interface [NativeWIFI]","HasProfile method","IDot11AdHocNetwork.HasProfile","IDot11AdHocNetwork::HasProfile","adhoc/IDot11AdHocNetwork::HasProfile","nwifi.idot11adhocnetwork_hasprofile"]
old-location: nwifi\idot11adhocnetwork_hasprofile.htm
tech.root: nwifi
ms.assetid: 252f32ef-0a54-445f-94ca-113a67a3e6dd
ms.date: 12/05/2018
ms.keywords: HasProfile, HasProfile method [NativeWIFI], HasProfile method [NativeWIFI],IDot11AdHocNetwork interface, IDot11AdHocNetwork interface [NativeWIFI],HasProfile method, IDot11AdHocNetwork.HasProfile, IDot11AdHocNetwork::HasProfile, adhoc/IDot11AdHocNetwork::HasProfile, nwifi.idot11adhocnetwork_hasprofile
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
 - IDot11AdHocNetwork::HasProfile
 - adhoc/IDot11AdHocNetwork::HasProfile
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
 - IDot11AdHocNetwork.HasProfile
---

# IDot11AdHocNetwork::HasProfile


## -description

Returns a boolean value that specifies whether there is a saved profile associated with the network.

## -parameters

### -param pf11d [in, out]

Specifies whether the network has a profile. This value is set to <b>TRUE</b> if the network has a profile and <b>FALSE</b> otherwise.

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

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a>



<a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-deleteprofile">IDot11AdHocNetwork::DeleteProfile</a>



<a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-getprofilename">IDot11AdHocNetwork::GetProfileName</a>
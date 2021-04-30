---
UID: NF:adhoc.IDot11AdHocManager.GetNetwork
title: IDot11AdHocManager::GetNetwork (adhoc.h)
description: Returns the network associated with a signature.
helpviewer_keywords: ["GetNetwork","GetNetwork method [NativeWIFI]","GetNetwork method [NativeWIFI]","IDot11AdHocManager interface","IDot11AdHocManager interface [NativeWIFI]","GetNetwork method","IDot11AdHocManager.GetNetwork","IDot11AdHocManager::GetNetwork","adhoc/IDot11AdHocManager::GetNetwork","nwifi.idot11adhocmanager_getnetwork"]
old-location: nwifi\idot11adhocmanager_getnetwork.htm
tech.root: nwifi
ms.assetid: 971703dc-1a3c-4c9a-a9e2-c547c96beacd
ms.date: 12/05/2018
ms.keywords: GetNetwork, GetNetwork method [NativeWIFI], GetNetwork method [NativeWIFI],IDot11AdHocManager interface, IDot11AdHocManager interface [NativeWIFI],GetNetwork method, IDot11AdHocManager.GetNetwork, IDot11AdHocManager::GetNetwork, adhoc/IDot11AdHocManager::GetNetwork, nwifi.idot11adhocmanager_getnetwork
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
 - IDot11AdHocManager::GetNetwork
 - adhoc/IDot11AdHocManager::GetNetwork
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
 - IDot11AdHocManager.GetNetwork
---

# IDot11AdHocManager::GetNetwork


## -description

Returns the network associated with a signature.

## -parameters

### -param NetworkSignature [in]

A signature that uniquely identifies an ad hoc network. This signature is generated  from certain network attributes.

### -param pNetwork [out]

A pointer to an <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a> interface that represents the network associated with the signature.

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
</table>

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a>
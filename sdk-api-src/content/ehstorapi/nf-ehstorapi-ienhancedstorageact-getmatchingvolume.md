---
UID: NF:ehstorapi.IEnhancedStorageACT.GetMatchingVolume
title: IEnhancedStorageACT::GetMatchingVolume (ehstorapi.h)
description: Returns the volume associated with the Addressable Command Target (ACT).
helpviewer_keywords: ["GetMatchingVolume","GetMatchingVolume method [Enhanced Storage]","GetMatchingVolume method [Enhanced Storage]","IEnhancedStorageACT interface","IEnhancedStorageACT interface [Enhanced Storage]","GetMatchingVolume method","IEnhancedStorageACT.GetMatchingVolume","IEnhancedStorageACT::GetMatchingVolume","ehstorapi/IEnhancedStorageACT::GetMatchingVolume","enstor.ienhancedstorageact_getmatchingvolume"]
old-location: enstor\ienhancedstorageact_getmatchingvolume.htm
tech.root: enstor
ms.assetid: aa5e5d33-0fc8-46bc-b1e8-c2bd341f0b4f
ms.date: 12/05/2018
ms.keywords: GetMatchingVolume, GetMatchingVolume method [Enhanced Storage], GetMatchingVolume method [Enhanced Storage],IEnhancedStorageACT interface, IEnhancedStorageACT interface [Enhanced Storage],GetMatchingVolume method, IEnhancedStorageACT.GetMatchingVolume, IEnhancedStorageACT::GetMatchingVolume, ehstorapi/IEnhancedStorageACT::GetMatchingVolume, enstor.ienhancedstorageact_getmatchingvolume
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
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
 - IEnhancedStorageACT::GetMatchingVolume
 - ehstorapi/IEnhancedStorageACT::GetMatchingVolume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EhStorAPI.h
api_name:
 - IEnhancedStorageACT.GetMatchingVolume
---

# IEnhancedStorageACT::GetMatchingVolume


## -description

Returns the volume associated with the Addressable Command Target (ACT).

## -parameters

### -param ppwszVolume [out]

Pointer to a string that represents the volume associated with the ACT.

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
The associated volume was successfully returned.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact">IEnhancedStorageACT</a>
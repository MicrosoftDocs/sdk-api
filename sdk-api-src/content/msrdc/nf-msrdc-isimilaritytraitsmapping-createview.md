---
UID: NF:msrdc.ISimilarityTraitsMapping.CreateView
title: ISimilarityTraitsMapping::CreateView (msrdc.h)
description: Maps a view of the file mapping for a similarity traits table file.
helpviewer_keywords: ["CreateView","CreateView method [Remote Differential Compression]","CreateView method [Remote Differential Compression]","ISimilarityTraitsMapping interface","ISimilarityTraitsMapping interface [Remote Differential Compression]","CreateView method","ISimilarityTraitsMapping.CreateView","ISimilarityTraitsMapping::CreateView","fs.isimilaritytraitsmapping_createview","msrdc/ISimilarityTraitsMapping::CreateView","rdc.isimilaritytraitsmapping_createview"]
old-location: rdc\isimilaritytraitsmapping_createview.htm
tech.root: rdc
ms.assetid: 222b3682-8ccc-4c52-858a-ad4ac8a65add
ms.date: 12/05/2018
ms.keywords: CreateView, CreateView method [Remote Differential Compression], CreateView method [Remote Differential Compression],ISimilarityTraitsMapping interface, ISimilarityTraitsMapping interface [Remote Differential Compression],CreateView method, ISimilarityTraitsMapping.CreateView, ISimilarityTraitsMapping::CreateView, fs.isimilaritytraitsmapping_createview, msrdc/ISimilarityTraitsMapping::CreateView, rdc.isimilaritytraitsmapping_createview
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimilarityTraitsMapping::CreateView
 - msrdc/ISimilarityTraitsMapping::CreateView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityTraitsMapping.CreateView
---

# ISimilarityTraitsMapping::CreateView


## -description

Maps a view of the file mapping for a similarity traits table file.

## -parameters

### -param minimumMappedPages [in]

Minimum number of pages of the file mapping to map to the view.

### -param accessMode [in]

<a href="/windows/win32/api/msrdc/ne-msrdc-rdcmappingaccessmode">RdcMappingAccessMode</a> enumeration value that specifies the desired access to the file mapping object.

### -param mappedView [out]

Pointer to a location that will receive the returned <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmappedview">ISimilarityTraitsMappedView</a> interface pointer. Callers must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Data accessed through read-only views will never be modified.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a>
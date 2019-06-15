---
UID: NF:msrdc.ISimilarityTraitsMapping.CreateView
title: ISimilarityTraitsMapping::CreateView (msrdc.h)
author: windows-sdk-content
description: Maps a view of the file mapping for a similarity traits table file.
old-location: rdc\isimilaritytraitsmapping_createview.htm
tech.root: rdc
ms.assetid: 222b3682-8ccc-4c52-858a-ad4ac8a65add
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateView, CreateView method [Remote Differential Compression], CreateView method [Remote Differential Compression],ISimilarityTraitsMapping interface, ISimilarityTraitsMapping interface [Remote Differential Compression],CreateView method, ISimilarityTraitsMapping.CreateView, ISimilarityTraitsMapping::CreateView, fs.isimilaritytraitsmapping_createview, msrdc/ISimilarityTraitsMapping::CreateView, rdc.isimilaritytraitsmapping_createview
ms.topic: method
f1_keywords: ["msrdc/ISimilarityTraitsMapping.CreateView"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityTraitsMapping.CreateView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISimilarityTraitsMapping::CreateView


## -description


Maps a view of the file mapping for a similarity traits table file.


## -parameters




### -param minimumMappedPages [in]

Minimum number of pages of the file mapping to map to the view.


### -param accessMode [in]


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/ne-msrdc-__midl___midl_itf_msrdc_0000_0000_0010">RdcMappingAccessMode</a> enumeration value that specifies the desired access to the file mapping object.


### -param mappedView [out]

Pointer to a location that will receive the returned <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmappedview">ISimilarityTraitsMappedView</a> interface pointer. Callers must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Data accessed through read-only views will never be modified.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a>
 

 


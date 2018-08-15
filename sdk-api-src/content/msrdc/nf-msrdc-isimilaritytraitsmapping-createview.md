---
UID: NF:msrdc.ISimilarityTraitsMapping.CreateView
title: ISimilarityTraitsMapping::CreateView
author: windows-sdk-content
description: Maps a view of the file mapping for a similarity traits table file.
old-location: rdc\isimilaritytraitsmapping_createview.htm
old-project: Rdc
ms.assetid: 222b3682-8ccc-4c52-858a-ad4ac8a65add
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: CreateView, CreateView method [Remote Differential Compression], CreateView method [Remote Differential Compression],ISimilarityTraitsMapping interface, ISimilarityTraitsMapping interface [Remote Differential Compression],CreateView method, ISimilarityTraitsMapping.CreateView, ISimilarityTraitsMapping::CreateView, fs.isimilaritytraitsmapping_createview, msrdc/ISimilarityTraitsMapping::CreateView, rdc.isimilaritytraitsmapping_createview
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RdcMappingAccessMode
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityTraitsMapping::CreateView


## -description


Maps a view of the file mapping for a similarity traits table file.


## -parameters




### -param minimumMappedPages [in]

Minimum number of pages of the file mapping to map to the view.


### -param accessMode [in]


<a href="https://msdn.microsoft.com/570fe290-1209-4bae-a56c-f6f663e53f87">RdcMappingAccessMode</a> enumeration value that specifies the desired access to the file mapping object.


### -param mappedView [out]

Pointer to a location that will receive the returned <a href="https://msdn.microsoft.com/48d6d4a0-fbf1-476a-b30f-83176c51cb48">ISimilarityTraitsMappedView</a> interface pointer. Callers must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Data accessed through read-only views will never be modified.




## -see-also




<a href="https://msdn.microsoft.com/1ddc599b-5a9b-4807-9005-00793f9a6ed4">ISimilarityTraitsMapping</a>
 

 


---
UID: NF:strmif.IFilterMapper2.CreateCategory
title: IFilterMapper2::CreateCategory
author: windows-sdk-content
description: The CreateCategory method adds a new filter category to the registry.
old-location: dshow\ifiltermapper2_createcategory.htm
old-project: DirectShow
ms.assetid: 37dc50a0-530c-4b31-b766-9e161b04c6d5
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CreateCategory, CreateCategory method [DirectShow], CreateCategory method [DirectShow],IFilterMapper2 interface, IFilterMapper2 interface [DirectShow],CreateCategory method, IFilterMapper2.CreateCategory, IFilterMapper2::CreateCategory, IFilterMapper2CreateCategory, dshow.ifiltermapper2_createcategory, strmif/IFilterMapper2::CreateCategory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterMapper2.CreateCategory
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterMapper2::CreateCategory


## -description



The <code>CreateCategory</code> method adds a new filter category to the registry.




## -parameters




### -param clsidCategory [in]

Class identifier (CLSID) of the new filter category.


### -param dwCategoryMerit [in]


<a href="https://msdn.microsoft.com/9e026675-e0a9-4c82-9b57-ab0e7d9592ea">Merit</a> of the category. Categories with higher merit are enumerated first.


### -param Description [in]

Descriptive name for the category.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



The filter graph manager initially skips all categories with a merit value less than or equal to MERIT_DO_NOT_USE, to speed up the graph-building process. Filter categories that should not be considered for playback should have a merit of MERIT_DO_NOT_USE or less.

A filter can appear in one or more categories (for example, Video Compressors) to restrict the search space.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2 Interface</a>
 

 


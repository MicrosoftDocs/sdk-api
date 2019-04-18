---
UID: NF:strmif.IFilterMapper.RegisterFilter
title: IFilterMapper::RegisterFilter (strmif.h)
author: windows-sdk-content
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Adds a filter to the registry; the filter can then be enumerated.
old-location: dshow\ifiltermapper_registerfilter.htm
tech.root: DirectShow
ms.assetid: e21da510-f4e6-417e-978d-bb53bf78cf94
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFilterMapper interface [DirectShow],RegisterFilter method, IFilterMapper.RegisterFilter, IFilterMapper::RegisterFilter, IFilterMapperRegisterFilter, RegisterFilter, RegisterFilter method [DirectShow], RegisterFilter method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_registerfilter, strmif/IFilterMapper::RegisterFilter
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IFilterMapper.RegisterFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFilterMapper::RegisterFilter


## -description



<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a> instead.</div>
<div> </div>
Adds a filter to the registry; the filter can then be enumerated.




## -parameters




### -param clsid [in]

Globally unique identifier (<b>GUID</b>) of the filter.


### -param Name [in]

Descriptive name for the filter.


### -param dwMerit [in]

Position in the order of enumeration. Filters with higher merit are enumerated first.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The merit (as defined by the <i>dwMerit</i> parameter) controls the order in which the filter graph manager tries filters when performing an operation as a result of a call to <a href="https://msdn.microsoft.com/8ddcbb73-8220-4d70-9ab3-58d99fa8a958">IGraphBuilder::Connect</a>, <a href="https://msdn.microsoft.com/de3adac7-ff99-4415-9afc-e25ad420df59">IGraphBuilder::Render</a>, or <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a>. The filter graph manager finds all filters registered with the correct media type and then tries the one with the highest merit, using other criteria in the registration to choose between filters with equal merit.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e2f32235-e331-4c3c-925a-7cfa531e9ab3">IFilterMapper Interface</a>
 

 


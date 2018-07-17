---
UID: NF:strmif.IFilterMapper.EnumMatchingFilters
title: IFilterMapper::EnumMatchingFilters
author: windows-sdk-content
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Provides an enumerator that enumerates registered filters that meet specified requirements.
old-location: dshow\ifiltermapper_enummatchingfilters.htm
old-project: DirectShow
ms.assetid: 602a7568-f5f8-4705-a2bc-6b9408bbbe54
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: EnumMatchingFilters, EnumMatchingFilters method [DirectShow], EnumMatchingFilters method [DirectShow],IFilterMapper interface, IFilterMapper interface [DirectShow],EnumMatchingFilters method, IFilterMapper.EnumMatchingFilters, IFilterMapper::EnumMatchingFilters, IFilterMapperEnumMatchingFilters, dshow.ifiltermapper_enummatchingfilters, strmif/IFilterMapper::EnumMatchingFilters
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IFilterMapper.EnumMatchingFilters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterMapper::EnumMatchingFilters


## -description



<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a> instead.</div>
<div> </div>
Provides an enumerator that enumerates registered filters that meet specified requirements.




## -parameters




### -param ppEnum [out]

Address of a pointer to the enumerator returned.


### -param dwMerit [in]

Minimum merit value of filters to enumerate.


### -param bInputNeeded

Value indicating whether there must be at least one input pin; <b>TRUE</b> indicates at least one input pin is required.


### -param clsInMaj [in]

Input major type required. Set to GUID_NULL if you do not care.


### -param clsInSub [in]

Input subtype required. Set to GUID_NULL if you do not care.


### -param bRender [in]

Flag that specifies whether the filter must render the input; <b>TRUE</b> means that it must.


### -param bOututNeeded




### -param clsOutMaj [in]

Output major type required. Set to GUID_NULL if you do not care.


### -param clsOutSub [in]

Output subtype required. Set to GUID_NULL if you do not care.


#### - bOutputNeeded [in]

Value indicating whether there must be at least one output pin; <b>TRUE</b> indicates at least one output pin is required.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Set the <i>ppEnum</i> parameter to be an enumerator for filters matching the requirements. For a description of merit values for the <i>dwMerit</i> parameter, see the <a href="https://msdn.microsoft.com/e21da510-f4e6-417e-978d-bb53bf78cf94">IFilterMapper::RegisterFilter</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e2f32235-e331-4c3c-925a-7cfa531e9ab3">IFilterMapper Interface</a>
 

 


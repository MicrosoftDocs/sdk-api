---
UID: NF:strmif.IFilterMapper.EnumMatchingFilters
title: IFilterMapper::EnumMatchingFilters (strmif.h)
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Provides an enumerator that enumerates registered filters that meet specified requirements.helpviewer_keywords: ["EnumMatchingFilters","EnumMatchingFilters method [DirectShow]","EnumMatchingFilters method [DirectShow]","IFilterMapper interface","IFilterMapper interface [DirectShow]","EnumMatchingFilters method","IFilterMapper.EnumMatchingFilters","IFilterMapper::EnumMatchingFilters","IFilterMapperEnumMatchingFilters","dshow.ifiltermapper_enummatchingfilters","strmif/IFilterMapper::EnumMatchingFilters"]
old-location: dshow\ifiltermapper_enummatchingfilters.htm
tech.root: DirectShow
ms.assetid: 602a7568-f5f8-4705-a2bc-6b9408bbbe54
ms.date: 12/05/2018
ms.keywords: EnumMatchingFilters, EnumMatchingFilters method [DirectShow], EnumMatchingFilters method [DirectShow],IFilterMapper interface, IFilterMapper interface [DirectShow],EnumMatchingFilters method, IFilterMapper.EnumMatchingFilters, IFilterMapper::EnumMatchingFilters, IFilterMapperEnumMatchingFilters, dshow.ifiltermapper_enummatchingfilters, strmif/IFilterMapper::EnumMatchingFilters
f1_keywords:
- strmif/IFilterMapper.EnumMatchingFilters
dev_langs:
- c++
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
- IFilterMapper.EnumMatchingFilters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFilterMapper::EnumMatchingFilters


## -description



<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> instead.</div>
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


### -param bOututNeeded [in]

Value indicating whether there must be at least one output pin; <b>TRUE</b> indicates at least one output pin is required.


### -param clsOutMaj [in]

Output major type required. Set to GUID_NULL if you do not care.


### -param clsOutSub [in]

Output subtype required. Set to GUID_NULL if you do not care.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Set the <i>ppEnum</i> parameter to be an enumerator for filters matching the requirements. For a description of merit values for the <i>dwMerit</i> parameter, see the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper-registerfilter">IFilterMapper::RegisterFilter</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper Interface</a>
 

 


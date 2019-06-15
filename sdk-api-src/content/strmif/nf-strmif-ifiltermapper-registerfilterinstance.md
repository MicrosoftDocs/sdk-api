---
UID: NF:strmif.IFilterMapper.RegisterFilterInstance
title: IFilterMapper::RegisterFilterInstance (strmif.h)
author: windows-sdk-content
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Registers an identifiable instance of a filter.
old-location: dshow\ifiltermapper_registerfilterinstance.htm
tech.root: DirectShow
ms.assetid: ce42047c-0b74-4ad4-b5a1-ea66fc6bffc3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFilterMapper interface [DirectShow],RegisterFilterInstance method, IFilterMapper.RegisterFilterInstance, IFilterMapper::RegisterFilterInstance, IFilterMapperRegisterFilterInstance, RegisterFilterInstance, RegisterFilterInstance method [DirectShow], RegisterFilterInstance method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_registerfilterinstance, strmif/IFilterMapper::RegisterFilterInstance
ms.topic: method
f1_keywords: ["strmif/IFilterMapper.RegisterFilterInstance"]
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
 - IFilterMapper.RegisterFilterInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFilterMapper::RegisterFilterInstance


## -description



<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> instead.</div>
<div> </div>
Registers an identifiable instance of a filter.




## -parameters




### -param clsid [in]

GUID of the filter.


### -param Name [in]

Descriptive name of the instance.


### -param MRId [out]

Pointer to the returned media resource ID. This parameter is a locally unique identifier for this instance of this filter.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method handles cases such as when two similar sound cards that are driven by the same driver are available, and it is necessary to choose which card will emit the sound. This is not needed if there is only one instance of the filter (such as when there is only one sound card in the computer), or if all instances of the filter are equivalent.

The filter itself must have already been registered.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper Interface</a>
 

 


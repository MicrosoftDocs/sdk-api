---
UID: NF:strmif.IFilterMapper.RegisterPin
title: IFilterMapper::RegisterPin
author: windows-sdk-content
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Records the details of the pin in the registry.
old-location: dshow\ifiltermapper_registerpin.htm
tech.root: DirectShow
ms.assetid: 9fd0072f-e63f-41e2-b8f1-821c3c0e0f4e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFilterMapper interface [DirectShow],RegisterPin method, IFilterMapper.RegisterPin, IFilterMapper::RegisterPin, IFilterMapperRegisterPin, RegisterPin, RegisterPin method [DirectShow], RegisterPin method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_registerpin, strmif/IFilterMapper::RegisterPin
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFilterMapper.RegisterPin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFilterMapper::RegisterPin


## -description



<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a> instead.</div>
<div> </div>
Records the details of the pin in the registry.




## -parameters




### -param Filter [in]

GUID of the filter.


### -param Name [in]

Name of the pin. This should be unique within the filter. It has no significance other than to indicate type information. You should not use pin names longer than 99 characters, because this causes filter enumeration problems.


### -param bRendered [in]

Value specifying whether the filter renders this input. Set to <b>TRUE</b> if it does; otherwise, set to <b>FALSE</b>.


### -param bOutput [in]

Value specifying whether this is an output pin. Set to <b>TRUE</b> if it is; otherwise, set to <b>FALSE</b>.


### -param bZero [in]

Value specifying whether the filter can have zero instances of this pin. If it can, set to <b>TRUE</b>; otherwise, set to <b>FALSE</b>. For example, a decompression filter doesn't need to create a sound output pin for a movie without a sound track.


### -param bMany [in]

Value specifying whether the filter can have many instances of this pin. If it can, set to <b>TRUE</b>; otherwise, set to <b>FALSE</b>. For example, a mixer might have multiple instances of its input pin.


### -param ConnectsToFilter [in]

Reserved. Must be <b>NULL</b>. (This is intended for filters such as system-wide mixers that have connections outside the filter graph. It is not yet implemented.)


### -param ConnectsToPin [in]

Reserved. Must be <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e2f32235-e331-4c3c-925a-7cfa531e9ab3">IFilterMapper Interface</a>
 

 


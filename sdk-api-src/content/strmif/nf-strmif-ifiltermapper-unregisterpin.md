---
UID: NF:strmif.IFilterMapper.UnregisterPin
title: IFilterMapper::UnregisterPin method
author: windows-driver-content
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Removes the registration of this pin from the registry.
old-location: dshow\ifiltermapper_unregisterpin.htm
old-project: DirectShow
ms.assetid: f8964890-53d7-4731-91b2-156e61809774
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IFilterMapper, IFilterMapper interface [DirectShow], UnregisterPin method, IFilterMapper::UnregisterPin, IFilterMapperUnregisterPin, UnregisterPin method [DirectShow], UnregisterPin method [DirectShow], IFilterMapper interface, UnregisterPin,IFilterMapper.UnregisterPin, dshow.ifiltermapper_unregisterpin, strmif/IFilterMapper::UnregisterPin
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IFilterMapper.UnregisterPin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterMapper::UnregisterPin method


## -description



<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a> instead.</div>
<div> </div>
Removes the registration of this pin from the registry.




## -parameters




### -param Filter [in]

GUID of the filter that this pin is part of.


### -param Name [in]

Name of the pin.


## -returns



Returns an <b>HRESULT</b> value.




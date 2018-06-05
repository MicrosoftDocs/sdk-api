---
UID: NF:strmif.IFilterMapper.RegisterPinType
title: IFilterMapper::RegisterPinType
author: windows-sdk-content
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Registers this pin type.
old-location: dshow\ifiltermapper_registerpintype.htm
old-project: DirectShow
ms.assetid: 7f92745b-2b97-4cc6-9755-a580827b5bba
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IFilterMapper interface [DirectShow],RegisterPinType method, IFilterMapper.RegisterPinType, IFilterMapper::RegisterPinType, IFilterMapperRegisterPinType, RegisterPinType, RegisterPinType method [DirectShow], RegisterPinType method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_registerpintype, strmif/IFilterMapper::RegisterPinType
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IFilterMapper.RegisterPinType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterMapper::RegisterPinType


## -description



<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a> instead.</div>
<div> </div>
Registers this pin type.




## -parameters




### -param clsFilter

Class identifier (CLSID) of the filter to which the pin belongs.


### -param strName

Name by which it is known.


### -param clsMajorType

Major type of the media sample supported by this pin class.


### -param clsSubType

Subtype of the media sample supported by this pin class.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The <i>clsMajorType</i> and <i>clsSubType</i> parameters specify the media type of the pin and correspond to the <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure's <b>majortype</b> and <b>subtype</b> members, respectively.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e2f32235-e331-4c3c-925a-7cfa531e9ab3">IFilterMapper Interface</a>
 

 


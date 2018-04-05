---
UID: NF:dmoimpl.IMediaObjectImpl.InputType
title: IMediaObjectImpl::InputType method
author: windows-driver-content
description: The InputType method retrieves the current media type for a specified input stream.
old-location: dshow\imediaobjectimpl_inputtype.htm
old-project: DirectShow
ms.assetid: e595ac21-14e0-45ae-a286-7938ad0e0a02
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMediaObjectImpl, IMediaObjectImpl interface [DirectShow], InputType method, IMediaObjectImpl::InputType, IMediaObjectImplInputType, InputType method [DirectShow], InputType method [DirectShow], IMediaObjectImpl interface, InputType,IMediaObjectImpl.InputType, dmoimpl/IMediaObjectImpl::InputType, dshow.imediaobjectimpl_inputtype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dmoimpl.h
req.include-header: 
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dmoguids.lib
-	Dmoguids.dll
-	Msdmo.lib
-	Msdmo.dll
api_name:
-	IMediaObjectImpl.InputType
product: Windows
targetos: Windows
req.lib: Dmoguids.lib; Msdmo.lib
req.dll: 
req.irql: 
---

# IMediaObjectImpl::InputType method


## -description



The <code>InputType</code> method retrieves the current media type for a specified input stream.




## -parameters




### -param ulInputStreamIndex

Index of an input stream.


## -returns



Returns a pointer to a <a href="https://msdn.microsoft.com/c545ddf7-9797-45ab-a42a-d8550b598e98">DMO_MEDIA_TYPE</a> structure, or <b>NULL</b> if the media type is not set for this stream.




## -see-also




<a href="https://msdn.microsoft.com/81d45b8d-8373-4e42-b768-f6126feb935d">IMediaObjectImpl Class Template</a>
 

 


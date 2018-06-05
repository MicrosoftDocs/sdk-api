---
UID: NF:tuner.IComponentType.get_MediaType
title: IComponentType::get_MediaType
author: windows-sdk-content
description: The get_MediaType method retrieves the DirectShow AM_MEDIA_TYPE structure for the component.
old-location: mstv\icomponenttype_get_mediatype.htm
old-project: mstv
ms.assetid: ca13cfc0-3e51-41cd-9405-aaa96927a35c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get_MediaType method, IComponentType.get_MediaType, IComponentType::get_MediaType, IComponentTypeget_MediaType, get_MediaType, get_MediaType method [Microsoft TV Technologies], get_MediaType method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get_mediatype, tuner/IComponentType::get_MediaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IComponentType.get_MediaType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentType::get_MediaType


## -description



The <b>get_MediaType</b> method retrieves the DirectShow <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure for the component.




## -parameters




### -param MediaType






#### - pMediaType [out]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that will be filled in with the values associated with the current <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a>.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 


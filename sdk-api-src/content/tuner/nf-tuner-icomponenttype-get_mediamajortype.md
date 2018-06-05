---
UID: NF:tuner.IComponentType.get_MediaMajorType
title: IComponentType::get_MediaMajorType
author: windows-sdk-content
description: The get_MediaMajorType method retrieves the DirectShow media major type as a BSTR.
old-location: mstv\icomponenttype_get_mediamajortype.htm
old-project: mstv
ms.assetid: 4c1fc49d-acca-40fe-85cf-909092ceb5ef
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get_MediaMajorType method, IComponentType.get_MediaMajorType, IComponentType::get_MediaMajorType, IComponentTypeget_MediaMajorType, get_MediaMajorType, get_MediaMajorType method [Microsoft TV Technologies], get_MediaMajorType method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get_mediamajortype, tuner/IComponentType::get_MediaMajorType
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
-	IComponentType.get_MediaMajorType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentType::get_MediaMajorType


## -description



The <b>get_MediaMajorType</b> method retrieves the DirectShow media major type as a <b>BSTR</b>.




## -parameters




### -param MediaMajorType






#### - pMediaMajorType [out]

Pointer to a <b>BSTR</b> that will receive the GUID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 


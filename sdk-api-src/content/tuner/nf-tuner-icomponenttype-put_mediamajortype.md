---
UID: NF:tuner.IComponentType.put_MediaMajorType
title: IComponentType::put_MediaMajorType
author: windows-sdk-content
description: The put_MediaMajorType method sets the DirectShow media major type.
old-location: mstv\icomponenttype_put_mediamajortype.htm
old-project: mstv
ms.assetid: 455a51f4-eb01-437a-9cb9-6ff93a6cc76e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],put_MediaMajorType method, IComponentType.put_MediaMajorType, IComponentType::put_MediaMajorType, IComponentTypeput_MediaMajorType, mstv.icomponenttype_put_mediamajortype, put_MediaMajorType, put_MediaMajorType method [Microsoft TV Technologies], put_MediaMajorType method [Microsoft TV Technologies],IComponentType interface, tuner/IComponentType::put_MediaMajorType
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IComponentType.put_MediaMajorType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentType::put_MediaMajorType


## -description



The <b>put_MediaMajorType</b> method sets the DirectShow media major type.




## -parameters




### -param MediaMajorType [in]

<b>BSTR</b> that specifies the GUID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 


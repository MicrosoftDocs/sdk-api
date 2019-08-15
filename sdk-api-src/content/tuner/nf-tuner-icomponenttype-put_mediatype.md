---
UID: NF:tuner.IComponentType.put_MediaType
title: IComponentType::put_MediaType (tuner.h)
author: windows-sdk-content
description: The put_MediaType method sets the DirectShow AM_MEDIA_TYPE structure for the component.
old-location: mstv\icomponenttype_put_mediatype.htm
tech.root: mstv
ms.assetid: 6f77a391-232f-46ef-a028-763ebc706784
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],put_MediaType method, IComponentType.put_MediaType, IComponentType::put_MediaType, IComponentTypeput_MediaType, mstv.icomponenttype_put_mediatype, put_MediaType, put_MediaType method [Microsoft TV Technologies], put_MediaType method [Microsoft TV Technologies],IComponentType interface, tuner/IComponentType::put_MediaType
ms.topic: method
f1_keywords: 
 - "tuner/IComponentType.put_MediaType"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponentType.put_MediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponentType::put_MediaType


## -description



The <b>put_MediaType</b> method sets the DirectShow <b>AM_MEDIA_TYPE</b> structure for the component.




## -parameters




### -param MediaType [in]

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that specifies the major type, subtype, format, and so on.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>
 

 


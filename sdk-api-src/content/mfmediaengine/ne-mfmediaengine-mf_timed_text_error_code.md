---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# MF_TIMED_TEXT_ERROR_CODE enumeration


## -description


Specifies the kind error that occurred with a timed text track.


## -enum-fields




### -field MF_TIMED_TEXT_ERROR_CODE_NOERROR

No error occurred.


### -field MF_TIMED_TEXT_ERROR_CODE_FATAL

A fatal error occurred.


### -field MF_TIMED_TEXT_ERROR_CODE_DATA_FORMAT

An error occurred with the data format of the timed text track.


### -field MF_TIMED_TEXT_ERROR_CODE_NETWORK

A network error occurred when trying to load the timed text track.


### -field MF_TIMED_TEXT_ERROR_CODE_INTERNAL

An internal error occurred.


## -remarks



This enumeration is used to return error information  from the <a href="https://msdn.microsoft.com/D73D3ACC-BD9C-4340-8572-6D82E96D0BA8">IMFTimedTextTrack::GetErrorCode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 


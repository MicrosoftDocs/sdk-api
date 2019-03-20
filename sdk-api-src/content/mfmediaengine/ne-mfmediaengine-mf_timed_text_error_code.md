---
UID: NE:mfmediaengine.MF_TIMED_TEXT_ERROR_CODE
title: MF_TIMED_TEXT_ERROR_CODE (mfmediaengine.h)
author: windows-sdk-content
description: Specifies the kind error that occurred with a timed text track.
old-location: mf\mf_timed_text_error_code.htm
tech.root: medfound
ms.assetid: D59B2063-5632-4115-BA8C-503181B5DF08
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MF_TIMED_TEXT_ERROR_CODE, MF_TIMED_TEXT_ERROR_CODE enumeration [Media Foundation], MF_TIMED_TEXT_ERROR_CODE_DATA_FORMAT, MF_TIMED_TEXT_ERROR_CODE_FATAL, MF_TIMED_TEXT_ERROR_CODE_INTERNAL, MF_TIMED_TEXT_ERROR_CODE_NETWORK, MF_TIMED_TEXT_ERROR_CODE_NOERROR, mf.mf_timed_text_error_code, mfmediaengine/MF_TIMED_TEXT_ERROR_CODE, mfmediaengine/MF_TIMED_TEXT_ERROR_CODE_DATA_FORMAT, mfmediaengine/MF_TIMED_TEXT_ERROR_CODE_FATAL, mfmediaengine/MF_TIMED_TEXT_ERROR_CODE_INTERNAL, mfmediaengine/MF_TIMED_TEXT_ERROR_CODE_NETWORK, mfmediaengine/MF_TIMED_TEXT_ERROR_CODE_NOERROR
ms.topic: enum
req.header: mfmediaengine.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfmediaengine.h
api_name:
 - MF_TIMED_TEXT_ERROR_CODE
product: Windows
targetos: Windows
req.typenames: MF_TIMED_TEXT_ERROR_CODE
req.redist: 
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
 

 


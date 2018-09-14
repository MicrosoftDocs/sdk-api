---
UID: NF:mfmediaengine.IMFTimedTextNotify.Error
title: IMFTimedTextNotify::Error
author: windows-sdk-content
description: Called when an error occurs in a text track.
old-location: mf\imftimedtextnotify_error.htm
tech.root: medfound
ms.assetid: 3658EE26-497D-4D33-BE68-572BCE1B28B1
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: Error, Error method [Media Foundation], Error method [Media Foundation],IMFTimedTextNotify interface, IMFTimedTextNotify interface [Media Foundation],Error method, IMFTimedTextNotify.Error, IMFTimedTextNotify::Error, mf.imftimedtextnotify_error, mfmediaengine/IMFTimedTextNotify::Error
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFTimedTextNotify.Error
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextNotify::Error


## -description


Called when an error occurs in a text track.


## -parameters




### -param errorCode [in]

Type: <b><a href="https://msdn.microsoft.com/D59B2063-5632-4115-BA8C-503181B5DF08">MF_TIMED_TEXT_ERROR_CODE</a></b>

An MF_TIMED_TEXT_ERROR_CODE representing the last error.


### -param extendedErrorCode

TBD


### -param sourceTrackId [in]

Type: <b>extendedErrorCode</b>

The identifier of the track on which the error occurred.


#### - HRESULT [in]

Type: <b>extendedErrorCode</b>

The extended error code for the last error.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/FE782D90-8CD4-4F8B-A20E-CE3F792A2DB4">IMFTimedTextNotify</a>
 

 


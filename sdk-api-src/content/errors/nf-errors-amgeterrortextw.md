---
UID: NF:errors.AMGetErrorTextW
title: AMGetErrorTextW function
author: windows-sdk-content
description: The AMGetErrorText function retrieves the error message for a given return code, using the current language setting.
old-location: dshow\amgeterrortext.htm
tech.root: DirectShow
ms.assetid: 268fd554-99f4-4400-8e33-4d98c51b76cf
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AMGetErrorText, AMGetErrorText function [DirectShow], AMGetErrorTextA, AMGetErrorTextW, dshow.amgeterrortext, errors/AMGetErrorText
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: errors.h
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
req.lib: Quartz.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Quartz.lib
 - Quartz.dll
api_name:
 - AMGetErrorText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AMGetErrorTextW function


## -description



The <b>AMGetErrorText</b> function retrieves the error message for a given return code, using the current language setting.



This function converts <b>HRESULT</b> return codes to error messages. The constant MAX_ERROR_TEXT_LEN specifies the maximum number of characters in an error message.


## -parameters




### -param hr

<b>HRESULT</b> value.


### -param pbuffer

TBD


### -param MaxLen

Number of characters in <i>pBuffer</i>.


#### - pBuffer

Pointer to a character buffer that receives the error message.


## -returns



Returns the number of characters returned in the buffer, or zero if an error occurred.




## -see-also




<a href="https://msdn.microsoft.com/5bf62e2a-7d5f-4feb-872a-54d102759824">Functions</a>
 

 


---
UID: NF:errors.AMGetErrorTextA
title: AMGetErrorTextA function (errors.h)
description: The AMGetErrorText function retrieves the error message for a given return code, using the current language setting.helpviewer_keywords: ["AMGetErrorText","AMGetErrorText function [DirectShow]","AMGetErrorTextA","AMGetErrorTextW","dshow.amgeterrortext","errors/AMGetErrorText"]
old-location: dshow\amgeterrortext.htm
tech.root: DirectShow
ms.assetid: 268fd554-99f4-4400-8e33-4d98c51b76cf
ms.date: 12/05/2018
ms.keywords: AMGetErrorText, AMGetErrorText function [DirectShow], AMGetErrorTextA, AMGetErrorTextW, dshow.amgeterrortext, errors/AMGetErrorText
f1_keywords:
- errors/AMGetErrorText
dev_langs:
- c++
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
- AMGetErrorTextA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AMGetErrorTextA function


## -description



The <b>AMGetErrorText</b> function retrieves the error message for a given return code, using the current language setting.



This function converts <b>HRESULT</b> return codes to error messages. The constant MAX_ERROR_TEXT_LEN specifies the maximum number of characters in an error message.


## -parameters




### -param hr

<b>HRESULT</b> value.


### -param pbuffer

Pointer to a character buffer that receives the error message.


### -param MaxLen

Number of characters in <i>pBuffer</i>.


## -returns



Returns the number of characters returned in the buffer, or zero if an error occurred.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/functions">Functions</a>
 

 


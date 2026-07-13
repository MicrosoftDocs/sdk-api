---
UID: NF:errors.AMGetErrorTextW
title: AMGetErrorTextW function (errors.h)
description: The AMGetErrorText function retrieves the error message for a given return code, using the current language setting. (Unicode)
helpviewer_keywords: ["AMGetErrorText", "AMGetErrorText function [DirectShow]", "AMGetErrorTextW", "dshow.amgeterrortext", "errors/AMGetErrorText"]
old-location: dshow\amgeterrortext.htm
tech.root: dshow
ms.assetid: 268fd554-99f4-4400-8e33-4d98c51b76cf
ms.date: 12/05/2018
ms.keywords: AMGetErrorText, AMGetErrorText function [DirectShow], AMGetErrorTextA, AMGetErrorTextW, dshow.amgeterrortext, errors/AMGetErrorText
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AMGetErrorTextW
 - errors/AMGetErrorTextW
dev_langs:
 - c++
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
 - AMGetErrorTextW
---

# AMGetErrorTextW function


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

<a href="/windows/desktop/DirectShow/functions">Functions</a>

## -remarks

> [!NOTE]
> The errors.h header defines AMGetErrorText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

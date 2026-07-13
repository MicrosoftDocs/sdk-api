---
UID: NF:intshcut.TranslateURLW
title: TranslateURLW function (intshcut.h)
description: Applies common translations to a given URL string, creating a new URL string. (Unicode)
helpviewer_keywords: ["TRANSLATEURL_FL_GUESS_PROTOCOL", "TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL", "TranslateURL", "TranslateURL function [Windows Shell]", "TranslateURLW", "_win32_TranslateURL", "intshcut/TranslateURL", "intshcut/TranslateURLW", "shell.TranslateURL"]
old-location: shell\TranslateURL.htm
tech.root: shell
ms.assetid: 2f089f5a-4d7c-4bb7-961c-5c6e3e73c7b7
ms.date: 12/05/2018
ms.keywords: TRANSLATEURL_FL_GUESS_PROTOCOL, TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL, TranslateURL, TranslateURL function [Windows Shell], TranslateURLA, TranslateURLW, _win32_TranslateURL, intshcut/TranslateURL, intshcut/TranslateURLA, intshcut/TranslateURLW, shell.TranslateURL
req.header: intshcut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TranslateURLW (Unicode) and TranslateURLA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Url.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TranslateURLW
 - intshcut/TranslateURLW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Url.dll
api_name:
 - TranslateURL
 - TranslateURLA
 - TranslateURLW
---

# TranslateURLW function


## -description

Applies common translations to a given URL string, creating a new URL string.

## -parameters

### -param pcszURL

Type: <b>PCTSTR</b>

The address of the URL string to be translated.

### -param dwInFlags

Type: <b>DWORD</b>

The bit flags that specify how the URL string is to be translated. This value can be a combination of the following:



#### TRANSLATEURL_FL_GUESS_PROTOCOL

If the protocol scheme is not specified in the <i>pcszURL</i> parameter to <b>TranslateURL</b>, the system automatically chooses a scheme and adds it to the URL.



#### TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL

If the protocol scheme is not specified in the <i>pcszURL</i> parameter to 
        						<b>TranslateURL</b>, the system adds the default protocol to the URL.

### -param ppszTranslatedURL [out]

Type: <b>PTSTR*</b>

A pointer variable that receives the pointer to the newly created, translated URL string, if any. The <i>ppszTranslatedURL</i> parameter is valid only if the function returns S_OK.


##### - dwInFlags.TRANSLATEURL_FL_GUESS_PROTOCOL

If the protocol scheme is not specified in the <i>pcszURL</i> parameter to <b>TranslateURL</b>, the system automatically chooses a scheme and adds it to the URL.


##### - dwInFlags.TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL

If the protocol scheme is not specified in the <i>pcszURL</i> parameter to 
        						<b>TranslateURL</b>, the system adds the default protocol to the URL.

## -returns

Type: <b>HRESULT</b>

Returns S_OK upon success, or S_FALSE if the URL did not require translation. If an error occurs, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The flag combination passed in <i>dwInFlags</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the input pointers is invalid.

</td>
</tr>
</table>

## -remarks

This function does not validate the input URL string. A successful return value does not indicate that the URL strings are valid URLs.




> [!NOTE]
> The intshcut.h header defines TranslateURL as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).


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

# TranslateURLA function


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




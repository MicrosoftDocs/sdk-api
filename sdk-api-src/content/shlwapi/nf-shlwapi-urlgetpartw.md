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

# UrlGetPartW function


## -description


Accepts a URL string and returns a specified part of that URL.


## -parameters




### -param pszIn [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.


### -param pszOut [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives a null-terminated string with the specified part of the URL.


### -param pcchOut [in, out]

Type: <b>DWORD*</b>

A pointer to a value that, on entry, is set to the number of characters in the <i>pszOut</i> buffer. When this function returns successfully, the value depends on whether the function is successful or returns E_POINTER. For other return values, the value of this parameter is meaningless.


### -param dwPart

Type: <b>DWORD</b>

The flags that specify which part of the URL to retrieve. It can have one of the following values.



#### URL_PART_HOSTNAME

The host name.



#### URL_PART_PASSWORD

The password.



#### URL_PART_PORT

The port number.



#### URL_PART_QUERY

The query portion of the URL.



#### URL_PART_SCHEME

The URL scheme.



#### URL_PART_USERNAME

The username.


### -param dwFlags

Type: <b>DWORD</b>

A flag that can be set to keep the URL scheme, in addition to the part that is specified by <i>dwPart</i>.



#### URL_PARTFLAG_KEEPSCHEME

Keep the URL scheme.


##### - dwFlags.URL_PARTFLAG_KEEPSCHEME

Keep the URL scheme.


##### - dwPart.URL_PART_HOSTNAME

The host name.


##### - dwPart.URL_PART_PASSWORD

The password.


##### - dwPart.URL_PART_PORT

The port number.


##### - dwPart.URL_PART_QUERY

The query portion of the URL.


##### - dwPart.URL_PART_SCHEME

The URL scheme.


##### - dwPart.URL_PART_USERNAME

The username.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful. The value pointed to by <i>pcchOut</i> will be set to the number of characters written to the output buffer, excluding the terminating <b>NULL</b>. If the buffer was too small, E_POINTER is returned, and the value pointed to by <i>pcchOut</i> will be set to the minimum number of characters that the buffer must be able to contain, including the terminating <b>NULL</b> character. Otherwise, a COM error value is returned.




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

# UrlIsW function


## -description


Tests whether a URL is a specified type.


## -parameters




### -param pszUrl [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.


### -param UrlIs

Type: <b>URLIS</b>

The type of URL to be tested for. This parameter can take one of the following values.



#### URLIS_APPLIABLE

Attempt to determine a valid scheme for the URL.



#### URLIS_DIRECTORY

Does the URL string end with a directory?



#### URLIS_FILEURL

Is the URL a file URL?



#### URLIS_HASQUERY

Does the URL have an appended query string?



#### URLIS_NOHISTORY

Is the URL a URL that is not typically tracked in navigation history?



#### URLIS_OPAQUE

Is the URL <a href="https://msdn.microsoft.com/460f4d41-2796-496d-9199-f2d1cd6e4a24">opaque</a>?



#### URLIS_URL

Is the URL valid?


##### - UrlIs.URLIS_APPLIABLE

Attempt to determine a valid scheme for the URL.


##### - UrlIs.URLIS_DIRECTORY

Does the URL string end with a directory?


##### - UrlIs.URLIS_FILEURL

Is the URL a file URL?


##### - UrlIs.URLIS_HASQUERY

Does the URL have an appended query string?


##### - UrlIs.URLIS_NOHISTORY

Is the URL a URL that is not typically tracked in navigation history?


##### - UrlIs.URLIS_OPAQUE

Is the URL <a href="https://msdn.microsoft.com/460f4d41-2796-496d-9199-f2d1cd6e4a24">opaque</a>?


##### - UrlIs.URLIS_URL

Is the URL valid?


## -returns



Type: <b>BOOL</b>

For all but one of the URL types, <b>UrlIs</b> returns <b>TRUE</b> if the URL is the specified type, or <b>FALSE</b> if not. 

                    

If <i>UrlIs</i> is set to <b>URLIS_APPLIABLE</b>, <b>UrlIs</b> will attempt to determine the URL scheme. If the function is able to determine a scheme, it returns <b>TRUE</b>, or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/b122d3e4-47cc-47c0-a30c-6f9d1aa9d174">UrlIsFileUrl</a>



<a href="https://msdn.microsoft.com/7602d2ef-1f21-4b2f-8ac9-195bb21d6ae7">UrlIsNoHistory</a>



<a href="https://msdn.microsoft.com/460f4d41-2796-496d-9199-f2d1cd6e4a24">UrlIsOpaque</a>
 

 


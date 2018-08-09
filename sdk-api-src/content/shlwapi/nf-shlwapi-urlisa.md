---
UID: NF:shlwapi.UrlIsA
title: UrlIsA function
author: windows-sdk-content
description: Tests whether a URL is a specified type.
old-location: shell\UrlIs.htm
old-project: shell
ms.assetid: 2e83c953-b4c5-4411-90ca-49ffb94ee374
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: URLIS_APPLIABLE, URLIS_DIRECTORY, URLIS_FILEURL, URLIS_HASQUERY, URLIS_NOHISTORY, URLIS_OPAQUE, URLIS_URL, UrlIs, UrlIs function [Windows Shell], UrlIsA, UrlIsW, _win32_UrlIs, shell.UrlIs, shlwapi/UrlIs, shlwapi/UrlIsA, shlwapi/UrlIsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlIsW (Unicode) and UrlIsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-url-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - UrlIs
 - UrlIsA
 - UrlIsW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# UrlIsA function


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


## -returns



Type: <b>BOOL</b>

For all but one of the URL types, <b>UrlIs</b> returns <b>TRUE</b> if the URL is the specified type, or <b>FALSE</b> if not. 

                    

If <i>UrlIs</i> is set to <b>URLIS_APPLIABLE</b>, <b>UrlIs</b> will attempt to determine the URL scheme. If the function is able to determine a scheme, it returns <b>TRUE</b>, or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/b122d3e4-47cc-47c0-a30c-6f9d1aa9d174">UrlIsFileUrl</a>



<a href="https://msdn.microsoft.com/7602d2ef-1f21-4b2f-8ac9-195bb21d6ae7">UrlIsNoHistory</a>



<a href="https://msdn.microsoft.com/460f4d41-2796-496d-9199-f2d1cd6e4a24">UrlIsOpaque</a>
 

 


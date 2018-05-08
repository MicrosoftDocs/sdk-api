---
UID: NF:shlwapi.PathIsContentTypeW
title: PathIsContentTypeW function
author: windows-driver-content
description: Determines if a file's registered content type matches the specified content type. This function obtains the content type for the specified file type and compares that string with the pszContentType. The comparison is not case-sensitive.
old-location: shell\PathIsContentType.htm
old-project: shell
ms.assetid: 53eac496-9666-41fc-8682-f7b6583a62fe
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: PathIsContentType, PathIsContentType function [Windows Shell], PathIsContentTypeA, PathIsContentTypeW, _win32_PathIsContentType, shell.PathIsContentType, shlwapi/PathIsContentType, shlwapi/PathIsContentTypeA, shlwapi/PathIsContentTypeW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsContentTypeW (Unicode) and PathIsContentTypeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
api_name:
-	PathIsContentType
-	PathIsContentTypeA
-	PathIsContentTypeW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathIsContentTypeW function


## -description


Determines if a file's registered content type matches the specified content type. This function obtains the content type for the specified file type and compares that string with the <i>pszContentType</i>. The comparison is not case-sensitive.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the file whose content type will be compared.


### -param pszContentType [in]

Type: <b>LPCTSTR</b>

The address of a character buffer that contains the null-terminated content type string to which the file's registered content type will be compared.


## -returns



Type: <b>BOOL</b>

Returns nonzero if the file's registered content type matches <i>pszContentType</i>, or zero otherwise.




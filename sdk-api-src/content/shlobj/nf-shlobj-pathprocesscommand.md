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

# PathProcessCommand function


## -description


Deprecated. Processes a string that contains a command line and generates a suitably quoted string, with arguments attached if required.


## -parameters




### -param pszSrc [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated string that contains the command line to process.


### -param pszDest [out]

Type: <b>PWSTR</b>

Pointer to a buffer that receives a null-terminated Unicode string with the appropriate quotation marks. To determine how large this buffer must be, set this parameter to <b>NULL</b>. The function returns the required buffer size.


### -param cchDest

TBD


### -param dwFlags

Type: <b>DWORD</b>

Flags that control the procedure. One or more of the following values:



#### PPCF_ADDQUOTES (0x00000001)

Add quotes if the path requires them.



#### PPCF_ADDARGUMENTS (0x00000003)

Append trailing arguments to the output string. This value includes <b>PPCF_ADDQUOTES</b>.



#### PPCF_NODIRECTORIES (0x00000010)

Do not match the input string against folders, only against file objects.



#### PPCF_FORCEQUALIFY (0x00000040)

Qualify even non-relative file names.



#### PPCF_LONGESTPOSSIBLE (0x00000080)

Always choose the longest possible executable name.


#### - iDestMax

Type: <b>int</b>

The maximum number of characters that can be put in <i>pszDest</i>, not including the terminating null character. If this value is too small, the function fails.


## -returns



Type: <b>LONG</b>

Returns a positive value if successful. If <i>lpDest</i> is set to <b>NULL</b>, the function returns the required buffer size in characters, including the terminating null character. If the call fails, the function returns a negative value.




## -remarks



<div class="alert"><b>Note</b>  This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It is not supported in Windows Vista and later versions of Windows.</div>
<div> </div>



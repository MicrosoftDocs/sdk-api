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

# MsiRecordGetStringW function


## -description


The 
<b>MsiRecordGetString</b> function returns the string value of a record field.


## -parameters




### -param hRecord [in]

Handle to the record.


### -param iField [in]

Specifies the field requested.


### -param szValueBuf [out]

Pointer to the buffer that receives the null terminated string containing the value of the record field. Do not attempt to determine the size of the buffer by passing in a null (value=0) for <i>szValueBuf</i>. You can get the size of the buffer by passing in an empty string (for example ""). The function then returns <b>ERROR_MORE_DATA</b> and <i>pcchValueBuf</i> contains the required buffer size in TCHARs, not including the terminating null character. On return of <b>ERROR_SUCCESS</b>, <i>pcchValueBuf</i> contains the number of <b>TCHARs</b> written to the buffer, not including the terminating null character.


### -param pcchValueBuf [in, out]

Pointer to the variable that specifies the size, in <b>TCHAR</b>s, of the buffer pointed to by the variable <i>szValueBuf</i>. When the function returns <b>ERROR_SUCCESS</b>, this variable contains the size of the data copied to <i>szValueBuf</i>, not including the terminating null character. If <i>szValueBuf</i> is not large enough, the function returns <b>ERROR_MORE_DATA</b> and stores the required size, not including the terminating null character, in the variable pointed to by <i>pcchValueBuf</i>.


## -returns



The 
<b>MsiRecordGetString</b> function returns one of the following values:




## -remarks



If <b>ERROR_MORE_DATA</b> is returned, the parameter which is a pointer gives the size of the buffer required to hold the string. If <b>ERROR_SUCCESS</b> is returned, it gives the number of characters written to the string buffer. To get the size of the buffer, pass in the address of a 1 character buffer as <i>szValueBuf</i> and specify the size of the buffer with <i>pcchValueBuf</i> as 0. This ensures that no string value returned by the function fits into the buffer. Do not attempt to determine the size of the buffer by passing in a Null (value=0).




## -see-also




<a href="https://msdn.microsoft.com/f566c4a4-b90c-4d73-9d7f-f5b836630636">Passing Null as the Argument of Windows Installer Functions</a>



<a href="database_functions.htm">Record Processing Functions</a>
 

 


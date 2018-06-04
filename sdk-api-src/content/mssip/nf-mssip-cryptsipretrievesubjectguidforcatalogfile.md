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

# CryptSIPRetrieveSubjectGuidForCatalogFile function


## -description


The  <b>CryptSIPRetrieveSubjectGuidForCatalogFile</b> function retrieves the subject GUID associated with the specified file.


## -parameters




### -param FileName [in]

The name of the file. If the <i>hFileIn</i> parameter is set, the value in this parameter is ignored.


### -param hFileIn [in, optional]

A handle to the file to check. This parameter must contain a valid handle if the <i>FileName</i> parameter is <b>NULL</b>. 



### -param pgSubject [out]

A globally unique ID that identifies the subject.


## -returns



The return value is <b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>.


If this function returns <b>FALSE</b>, additional error information can be obtained by calling the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. <b>GetLastError</b> will return one of the following error codes.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are not valid.

</td>
</tr>
</table>
 




## -remarks



This function only supports <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface packages</a> (SIPs) that are used for portable executable images (.exe), cabinet (.cab) images, and flat files.




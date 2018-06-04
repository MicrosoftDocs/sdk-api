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

# IBackgroundCopyError::GetFile


## -description


Retrieves an interface pointer to the file object associated with the error.


## -parameters




### -param pVal






#### - ppFile [out]

An <a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a> interface pointer whose methods you use to determine the local and remote file names associated with the error. The <i>ppFile</i> parameter is set to <b>NULL</b> if the error is not associated with the local or remote file. When done, release <i>ppFile</i>.


## -returns



This method returns the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved an interface pointer to the file object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_FILE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The error is not associated with a local or remote file. The <i>ppFile</i> parameter is set to <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/abdf115d-3ff2-4664-b053-f55872ad24ab">IBackgroundCopyError::GetError</a>



<a href="https://msdn.microsoft.com/87f5ae62-c171-4637-bebb-3a5c5aa546b3">IBackgroundCopyError::GetErrorContextDescription</a>



<a href="https://msdn.microsoft.com/57323f38-c2e6-4e40-b357-7df758899f97">IBackgroundCopyError::GetErrorDescription</a>
 

 


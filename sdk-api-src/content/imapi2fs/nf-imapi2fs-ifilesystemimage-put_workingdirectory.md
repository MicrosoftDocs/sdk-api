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

# IFileSystemImage::put_WorkingDirectory


## -description


Sets the temporary directory in which stash files are built. 


## -parameters




### -param newVal [in]

String that contains the path to the temporary working directory. The default is the current temp directory.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_WORKING_DIRECTORY</b></dt>
</dl>
</td>
<td width="60%">
The working directory <i>%1!ls!</i> is not valid.

Value: 0xC0AAB140

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_WORKING_DIRECTORY_SPACE</b></dt>
</dl>
</td>
<td width="60%">
Cannot set working directory to <i>%1!ls!</i>. Space available is <i>%2!I64d!</i> bytes, approximately <i>%3!I64d!</i> bytes required. 

Value: 0xC0AAB141

</td>
</tr>
</table>
 




## -remarks



  
Stash files are the temporary files used to build the file-system image.

An exception results if the existing stash files cannot move to the new working directory. 

You cannot change the working directory if a result stream exists for the file-system image.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/89c4fd34-6651-4056-9939-201f404ea6ee">IFileSystemImage::get_WorkingDirectory</a>
 

 


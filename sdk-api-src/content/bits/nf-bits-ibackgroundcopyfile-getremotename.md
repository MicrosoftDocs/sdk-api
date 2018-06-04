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

# IBackgroundCopyFile::GetRemoteName


## -description


Retrieves the remote name of the file.


## -parameters




### -param pVal






#### - ppName [out]

Null-terminated string that contains the remote name of the file to transfer. The name is fully qualified. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppName</i> when done.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -remarks



The remote file name is set when you call the 
<a href="https://msdn.microsoft.com/0dada1d3-49b6-41af-b17f-612f27ea4d56">AddFile</a> or 
<a href="https://msdn.microsoft.com/fe2f9b47-0f0a-48ab-be0e-658307cfec5f">AddFileSet</a> methods of the 
<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> interface.

To change the remote file name, call the <a href="https://msdn.microsoft.com/6dd33b7d-4317-4eb5-aae4-83d3f4416bf9">IBackgroundCopyFile2::SetRemoteName</a> method or the <a href="https://msdn.microsoft.com/5ea62d29-c40e-4bd2-b22a-fce2d9f4eecf">IBackgroundCopyJob3::ReplaceRemotePrefix</a> method.


#### Examples

See the example code for the 
<a href="https://msdn.microsoft.com/d27844b7-a5c6-4f4c-a1db-80e031898634">IBackgroundCopyFile::GetLocalName</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/d27844b7-a5c6-4f4c-a1db-80e031898634">IBackgroundCopyFile::GetLocalName</a>



<a href="https://msdn.microsoft.com/0dada1d3-49b6-41af-b17f-612f27ea4d56">IBackgroundCopyJob::AddFile</a>



<a href="https://msdn.microsoft.com/fe2f9b47-0f0a-48ab-be0e-658307cfec5f">IBackgroundCopyJob::AddFileSet</a>
 

 


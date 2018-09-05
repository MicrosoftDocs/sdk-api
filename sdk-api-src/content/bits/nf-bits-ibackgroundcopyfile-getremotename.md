---
UID: NF:bits.IBackgroundCopyFile.GetRemoteName
title: IBackgroundCopyFile::GetRemoteName
author: windows-sdk-content
description: Retrieves the remote name of the file.
old-location: bits\ibackgroundcopyfile_getremotename.htm
old-project: bits
ms.assetid: b6b1b1dc-776e-4369-bd39-d159e4edfe38
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetRemoteName, GetRemoteName method [BITS], GetRemoteName method [BITS],IBackgroundCopyFile interface, IBackgroundCopyFile interface [BITS],GetRemoteName method, IBackgroundCopyFile.GetRemoteName, IBackgroundCopyFile::GetRemoteName, _drz_ibackgroundcopyfile_getremotename, bits.ibackgroundcopyfile_getremotename, bits/IBackgroundCopyFile::GetRemoteName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyFile.GetRemoteName
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
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
 

 


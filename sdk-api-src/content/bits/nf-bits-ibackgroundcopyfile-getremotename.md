---
UID: NF:bits.IBackgroundCopyFile.GetRemoteName
title: IBackgroundCopyFile::GetRemoteName
author: windows-sdk-content
description: Retrieves the remote name of the file.
old-location: bits\ibackgroundcopyfile_getremotename.htm
tech.root: Bits
ms.assetid: b6b1b1dc-776e-4369-bd39-d159e4edfe38
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRemoteName, GetRemoteName method [BITS], GetRemoteName method [BITS],IBackgroundCopyFile interface, IBackgroundCopyFile interface [BITS],GetRemoteName method, IBackgroundCopyFile.GetRemoteName, IBackgroundCopyFile::GetRemoteName, _drz_ibackgroundcopyfile_getremotename, bits.ibackgroundcopyfile_getremotename, bits/IBackgroundCopyFile::GetRemoteName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits.h
req.include-header: 
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
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# IBackgroundCopyFile::GetRemoteName


## -description


Retrieves the remote name of the file.


## -parameters




### -param pVal

TBD




#### - ppName [out]

Null-terminated string that contains the remote name of the file to transfer. The name is fully qualified. Call the 
<a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function to free <i>ppName</i> when done.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -remarks



The remote file name is set when you call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363017(v=VS.85).aspx">AddFile</a> or 
<a href="https://msdn.microsoft.com/en-us/library/Aa363019(v=VS.85).aspx">AddFileSet</a> methods of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a> interface.

To change the remote file name, call the <a href="https://msdn.microsoft.com/en-us/library/Aa362948(v=VS.85).aspx">IBackgroundCopyFile2::SetRemoteName</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa362993(v=VS.85).aspx">IBackgroundCopyJob3::ReplaceRemotePrefix</a> method.


#### Examples

See the example code for the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362956(v=VS.85).aspx">IBackgroundCopyFile::GetLocalName</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362881(v=VS.85).aspx">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362956(v=VS.85).aspx">IBackgroundCopyFile::GetLocalName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363017(v=VS.85).aspx">IBackgroundCopyJob::AddFile</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363019(v=VS.85).aspx">IBackgroundCopyJob::AddFileSet</a>
 

 


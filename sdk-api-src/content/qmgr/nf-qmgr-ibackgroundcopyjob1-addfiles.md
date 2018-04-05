---
UID: NF:qmgr.IBackgroundCopyJob1.AddFiles
title: IBackgroundCopyJob1::AddFiles method
author: windows-driver-content
description: Use the AddFiles method to add one or more files to download to the job.
old-location: bits\ibackgroundcopyjob1_addfiles.htm
old-project: Bits
ms.assetid: 4a9860da-3977-4b97-957f-dd4de1e775cb
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: AddFiles method [BITS], AddFiles method [BITS], IBackgroundCopyJob1 interface, AddFiles,IBackgroundCopyJob1.AddFiles, IBackgroundCopyJob1, IBackgroundCopyJob1 interface [BITS], AddFiles method, IBackgroundCopyJob1::AddFiles, bits.ibackgroundcopyjob1_addfiles, qmgr/IBackgroundCopyJob1::AddFiles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: GROUPPROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyJob1.AddFiles
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IBackgroundCopyJob1::AddFiles method


## -description


<p class="CCE_Message">[<b>IBackgroundCopyJob1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>AddFiles</b> method to add one or more files to download to the job.


## -parameters




### -param cFileCount [in]

Number of files in <i>pFileInfo</i> to add to the job.


### -param ppFileSet






#### - pFileInfo [in]

Array of <a href="https://msdn.microsoft.com/1a1d6683-5317-4a34-828d-55142f64f19f">FILESETINFO</a> structures that contain the remote and local names of the files to download.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

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
Files were successfully added to the job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Local or remote file name is invalid. For example, the remote file name specifies an unsupported protocol.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
User does not have permission to write to the specified directory on the client.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ccf1b355-c1af-4b5e-b613-181c426ed777">IBackgroundCopyJob1</a>
 

 


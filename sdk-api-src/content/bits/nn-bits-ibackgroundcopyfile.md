---
UID: NN:bits.IBackgroundCopyFile
title: IBackgroundCopyFile
author: windows-sdk-content
description: IBackgroundCopyFile contains information about a file that is part of a job. For example, you can use IBackgroundCopyFile methods to retrieve the local and remote names of the file and transfer progress information.
old-location: bits\ibackgroundcopyfile.htm
old-project: Bits
ms.assetid: fae9cf56-c211-445b-b962-9a9d7d67c59c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IBackgroundCopyFile, IBackgroundCopyFile interface [BITS], IBackgroundCopyFile interface [BITS],described, _drz_ibackgroundcopyfile, bits.ibackgroundcopyfile, bits/IBackgroundCopyFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyFile
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyFile interface


## -description


<b>IBackgroundCopyFile</b> contains information about a file that is part of a job. For example, you can use <b>IBackgroundCopyFile</b> methods to retrieve the local and remote names of the file and transfer progress information.

To get an 
<b>IBackgroundCopyFile</b> interface pointer, call the 
<a href="https://msdn.microsoft.com/7b6d4bd4-2102-4e6b-b250-1d73fae94cf9">IBackgroundCopyError::GetFile</a> method or the 
<a href="https://msdn.microsoft.com/ac62533a-8949-41b9-a3e6-f9030884a9ce">IEnumBackgroundCopyFiles::Next</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBackgroundCopyFile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyFile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d27844b7-a5c6-4f4c-a1db-80e031898634">GetLocalName</a>
</td>
<td align="left" width="63%">
Retrieves the local name of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e72ec5af-7c21-48f8-b027-76a6c9e67f5e">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves the progress of the file transfer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6b1b1dc-776e-4369-bd39-d159e4edfe38">GetRemoteName</a>
</td>
<td align="left" width="63%">
Retrieves the remote name of the file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a0b9e887-84d5-4f67-a65c-6a807c50dafd">IBackgroundCopyError</a>



<a href="https://msdn.microsoft.com/facff24d-56a3-4a1f-a726-3442c17fe869">IBackgroundCopyFile2</a>



<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/831998ba-601c-43c4-ba27-faff741f8eb4">IEnumBackgroundCopyFiles</a>
 

 


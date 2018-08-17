---
UID: NN:bits.IBackgroundCopyFile
title: IBackgroundCopyFile
author: windows-sdk-content
description: IBackgroundCopyFile contains information about a file that is part of a job. For example, you can use IBackgroundCopyFile methods to retrieve the local and remote names of the file and transfer progress information.
old-location: bits\ibackgroundcopyfile.htm
old-project: bits
ms.assetid: fae9cf56-c211-445b-b962-9a9d7d67c59c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBackgroundCopyFile, IBackgroundCopyFile interface [BITS], IBackgroundCopyFile interface [BITS],described, _drz_ibackgroundcopyfile, bits.ibackgroundcopyfile, bits/IBackgroundCopyFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IBackgroundCopyFile
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
<a href="https://msdn.microsoft.com/en-us/library/Aa362879(v=VS.85).aspx">IBackgroundCopyError::GetFile</a> method or the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363100(v=VS.85).aspx">IEnumBackgroundCopyFiles::Next</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IBackgroundCopyFile</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa362956(v=VS.85).aspx">GetLocalName</a>
</td>
<td align="left" width="63%">
Retrieves the local name of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa362957(v=VS.85).aspx">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves the progress of the file transfer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa362958(v=VS.85).aspx">GetRemoteName</a>
</td>
<td align="left" width="63%">
Retrieves the remote name of the file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362875(v=VS.85).aspx">IBackgroundCopyError</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362944(v=VS.85).aspx">IBackgroundCopyFile2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363097(v=VS.85).aspx">IEnumBackgroundCopyFiles</a>
 

 


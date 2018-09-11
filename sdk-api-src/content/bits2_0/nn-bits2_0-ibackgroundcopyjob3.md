---
UID: NN:bits2_0.IBackgroundCopyJob3
title: IBackgroundCopyJob3
author: windows-sdk-content
description: Use the IBackgroundCopyJob3 interface to download ranges of a file and change the prefix of a remote file name.
old-location: bits\ibackgroundcopyjob3.htm
tech.root: bits
ms.assetid: 46e115bb-2634-4b79-b307-45720d8cb2be
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBackgroundCopyJob3, IBackgroundCopyJob3 interface [BITS], IBackgroundCopyJob3 interface [BITS],described, bits.ibackgroundcopyjob3, bits2_0/IBackgroundCopyJob3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bits2_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2,KB842773 on  Windows Server 2003, and  Windows XP
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx3.dll
api_name:
 - IBackgroundCopyJob3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob3 interface


## -description


Use the 
<b>IBackgroundCopyJob3</b> interface to download ranges of a file and change the prefix of a remote file name. 

The 
<b>IBackgroundCopyJob3</b> interface inherits from the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362981(v=VS.85).aspx">IBackgroundCopyJob2</a> interface. 

To get an 
<b>IBackgroundCopyJob3</b> interface pointer, call the <b>IBackgroundCopyJob::QueryInterface</b> method using <code>__uuidof(IBackgroundCopyJob3)</code> for the interface identifier. 

Use the 
<b>IBackgroundCopyJob3</b> interface pointer to call  the 
methods of the <a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>,  
<a href="https://msdn.microsoft.com/en-us/library/Aa362981(v=VS.85).aspx">IBackgroundCopyJob2</a>, and <b>IBackgroundCopyJob3</b> interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa362981(v=VS.85).aspx">IBackgroundCopyJob2</a>. <b>IBackgroundCopyJob3</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyJob3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa362991(v=VS.85).aspx">AddFileWithRanges</a>
</td>
<td align="left" width="63%">
Add a file to a download job and specify the ranges of the file you want to download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa362992(v=VS.85).aspx">GetFileACLFlags</a>
</td>
<td align="left" width="63%">
Retrieves the flags that identify the owner and ACL information to maintain when downloading a file using SMB.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa362993(v=VS.85).aspx">ReplaceRemotePrefix</a>
</td>
<td align="left" width="63%">
Use to replace the beginning text of all  remote names in the job with the given string. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa362994(v=VS.85).aspx">SetFileACLFlags</a>
</td>
<td align="left" width="63%">
Specifies the owner and ACL information to maintain when downloading a file using SMB.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362981(v=VS.85).aspx">IBackgroundCopyJob2</a>
 

 


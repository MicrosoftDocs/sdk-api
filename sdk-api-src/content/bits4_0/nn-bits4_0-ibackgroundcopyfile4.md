---
UID: NN:bits4_0.IBackgroundCopyFile4
title: IBackgroundCopyFile4 (bits4_0.h)
author: windows-sdk-content
description: Use this interface to retrieve download statistics for peers and origin servers.
old-location: bits\ibackgroundcopyfile4.htm
tech.root: Bits
ms.assetid: d404c4f8-cc97-4254-bca8-41bc359f0777
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile4, IBackgroundCopyFile4 interface [BITS], IBackgroundCopyFile4 interface [BITS],described, bits.ibackgroundcopyfile4, bits4_0/IBackgroundCopyFile4
ms.topic: interface
req.header: bits4_0.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits4_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits4_0.h
api_name:
 - IBackgroundCopyFile4
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on  Windows Vista with SP1,  Windows Vista with SP2, and  Windows Server 2008 with SP2
---

# IBackgroundCopyFile4 interface


## -description


Use this 
interface to retrieve download statistics for peers and origin servers.

To get an 
<b>IBackgroundCopyFile4</b> interface pointer, call the <b>IBackgroundCopyFile::QueryInterface</b> method using __uuidof(IBackgroundCopyFile4) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile4</b> interface inherits from <a href="https://msdn.microsoft.com/5304f93a-993a-4327-9fdb-fb2ef1dafecb">IBackgroundCopyFile3</a>. <b>IBackgroundCopyFile4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyFile4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dff90887-90d5-48a4-a400-31d99de27d39">GetPeerDownloadStats</a>
</td>
<td align="left" width="63%">
Specifies statistics about the amount of data downloaded from peers and origin servers.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/facff24d-56a3-4a1f-a726-3442c17fe869">IBackgroundCopyFile2</a>



<a href="https://msdn.microsoft.com/5304f93a-993a-4327-9fdb-fb2ef1dafecb">IBackgroundCopyFile3</a>
 

 


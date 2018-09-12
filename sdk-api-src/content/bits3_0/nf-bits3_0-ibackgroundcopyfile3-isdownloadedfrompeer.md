---
UID: NF:bits3_0.IBackgroundCopyFile3.IsDownloadedFromPeer
title: IBackgroundCopyFile3::IsDownloadedFromPeer
author: windows-sdk-content
description: Gets a value that determines if any part of the file was downloaded from a peer.
old-location: bits\ibackgroundcopyfile3_isdownloadedfrompeer.htm
tech.root: bits
ms.assetid: b6084cfe-b3ab-4c9f-b335-2696e5839451
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBackgroundCopyFile3 interface [BITS],IsDownloadedFromPeer method, IBackgroundCopyFile3.IsDownloadedFromPeer, IBackgroundCopyFile3::IsDownloadedFromPeer, IsDownloadedFromPeer, IsDownloadedFromPeer method [BITS], IsDownloadedFromPeer method [BITS],IBackgroundCopyFile3 interface, bits.ibackgroundcopyfile3_isdownloadedfrompeer, bits3_0/IBackgroundCopyFile3::IsDownloadedFromPeer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyFile3.IsDownloadedFromPeer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyFile3::IsDownloadedFromPeer


## -description


Gets a value that determines if any part of the file was downloaded from a peer.


## -parameters




### -param pVal

TBD




#### - pFromPeer [out]

Is <b>TRUE</b> if any part of the file was downloaded from a peer; otherwise, <b>FALSE</b>.


## -returns



The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5304f93a-993a-4327-9fdb-fb2ef1dafecb">IBackgroundCopyFile3</a>
 

 


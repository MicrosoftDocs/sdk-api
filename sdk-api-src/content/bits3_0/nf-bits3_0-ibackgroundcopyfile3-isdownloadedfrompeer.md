---
UID: NF:bits3_0.IBackgroundCopyFile3.IsDownloadedFromPeer
title: IBackgroundCopyFile3::IsDownloadedFromPeer (bits3_0.h)
description: Gets a value that determines if any part of the file was downloaded from a peer.
helpviewer_keywords: ["IBackgroundCopyFile3 interface [BITS]","IsDownloadedFromPeer method","IBackgroundCopyFile3.IsDownloadedFromPeer","IBackgroundCopyFile3::IsDownloadedFromPeer","IsDownloadedFromPeer","IsDownloadedFromPeer method [BITS]","IsDownloadedFromPeer method [BITS]","IBackgroundCopyFile3 interface","bits.ibackgroundcopyfile3_isdownloadedfrompeer","bits3_0/IBackgroundCopyFile3::IsDownloadedFromPeer"]
old-location: bits\ibackgroundcopyfile3_isdownloadedfrompeer.htm
tech.root: Bits
ms.assetid: b6084cfe-b3ab-4c9f-b335-2696e5839451
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile3 interface [BITS],IsDownloadedFromPeer method, IBackgroundCopyFile3.IsDownloadedFromPeer, IBackgroundCopyFile3::IsDownloadedFromPeer, IsDownloadedFromPeer, IsDownloadedFromPeer method [BITS], IsDownloadedFromPeer method [BITS],IBackgroundCopyFile3 interface, bits.ibackgroundcopyfile3_isdownloadedfrompeer, bits3_0/IBackgroundCopyFile3::IsDownloadedFromPeer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyFile3::IsDownloadedFromPeer
 - bits3_0/IBackgroundCopyFile3::IsDownloadedFromPeer
dev_langs:
 - c++
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
---

# IBackgroundCopyFile3::IsDownloadedFromPeer


## -description

Gets a value that determines if any part of the file was downloaded from a peer.

## -parameters

### -param pVal [out]

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

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopyfile3">IBackgroundCopyFile3</a>
---
UID: NF:qmgr.IBackgroundCopyJob1.GetFileCount
title: IBackgroundCopyJob1::GetFileCount (qmgr.h)
description: Use the GetFileCount method to retrieve the number of files in the job.
helpviewer_keywords: ["GetFileCount","GetFileCount method [BITS]","GetFileCount method [BITS]","IBackgroundCopyJob1 interface","IBackgroundCopyJob1 interface [BITS]","GetFileCount method","IBackgroundCopyJob1.GetFileCount","IBackgroundCopyJob1::GetFileCount","bits.ibackgroundcopyjob1_getfilecount","qmgr/IBackgroundCopyJob1::GetFileCount"]
old-location: bits\ibackgroundcopyjob1_getfilecount.htm
tech.root: Bits
ms.assetid: 6aec5e9c-2950-4039-99a4-b1884a9a4673
ms.date: 12/05/2018
ms.keywords: GetFileCount, GetFileCount method [BITS], GetFileCount method [BITS],IBackgroundCopyJob1 interface, IBackgroundCopyJob1 interface [BITS],GetFileCount method, IBackgroundCopyJob1.GetFileCount, IBackgroundCopyJob1::GetFileCount, bits.ibackgroundcopyjob1_getfilecount, qmgr/IBackgroundCopyJob1::GetFileCount
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
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob1::GetFileCount
 - qmgr/IBackgroundCopyJob1::GetFileCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob1.GetFileCount
---

# IBackgroundCopyJob1::GetFileCount


## -description

<p class="CCE_Message">[<b>IBackgroundCopyJob1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>GetFileCount</b> method to retrieve the number of files in the job.

## -parameters

### -param pdwFileCount [out]

Number of files in the job.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved the number of files in the job.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyjob1">IBackgroundCopyJob1</a>
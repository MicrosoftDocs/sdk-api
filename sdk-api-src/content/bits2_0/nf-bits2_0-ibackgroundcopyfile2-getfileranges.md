---
UID: NF:bits2_0.IBackgroundCopyFile2.GetFileRanges
title: IBackgroundCopyFile2::GetFileRanges
author: windows-sdk-content
description: Retrieves the ranges that you want to download from the remote file.
old-location: bits\ibackgroundcopyfile2_getfileranges.htm
old-project: bits
ms.assetid: 2e0ea08e-5f97-45c9-9280-ce6c4dce7a17
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetFileRanges, GetFileRanges method [BITS], GetFileRanges method [BITS],IBackgroundCopyFile2 interface, IBackgroundCopyFile2 interface [BITS],GetFileRanges method, IBackgroundCopyFile2.GetFileRanges, IBackgroundCopyFile2::GetFileRanges, bits.ibackgroundcopyfile2_getfileranges, bits2_0/IBackgroundCopyFile2::GetFileRanges
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits2_0.h
req.include-header: Bits.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2,KB842773 on  Windows Server 2003,  and Windows XP
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
tech.root: 
req.typenames: BG_AUTH_CREDENTIALS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx3.dll
api_name:
 - IBackgroundCopyFile2.GetFileRanges
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: BitsPrx3.dll
req.irql: 
---

# IBackgroundCopyFile2::GetFileRanges


## -description


Retrieves the ranges that you want to download from the remote file.


## -parameters




### -param RangeCount [in, out]

Number of elements in <i>Ranges</i>.


### -param Ranges [out]

Array of  <a href="https://msdn.microsoft.com/en-us/library/Aa362802(v=VS.85).aspx">BG_FILE_RANGE</a> structures that specify the ranges to download. When done, call the <a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function to free <i>Ranges</i>.


## -returns



This method returns the following return values, as well as others.

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
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No ranges were specified or the job is an upload or upload-reply job. <i>RangeCount</i> is set to zero and <i>Ranges</i> is set to <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362802(v=VS.85).aspx">BG_FILE_RANGE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362944(v=VS.85).aspx">IBackgroundCopyFile2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362991(v=VS.85).aspx">IBackgroundCopyJob3::AddFileWithRanges</a>
 

 


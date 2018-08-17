---
UID: NF:bits.IEnumBackgroundCopyFiles.Skip
title: IEnumBackgroundCopyFiles::Skip
author: windows-sdk-content
description: Skips the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.
old-location: bits\ienumbackgroundcopyfiles_skip.htm
old-project: bits
ms.assetid: 41488586-cb91-4b87-b11d-2808bc162d42
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IEnumBackgroundCopyFiles interface [BITS],Skip method, IEnumBackgroundCopyFiles.Skip, IEnumBackgroundCopyFiles::Skip, Skip, Skip method [BITS], Skip method [BITS],IEnumBackgroundCopyFiles interface, _drz_ienumbackgroundcopyfiles_skip, bits.ienumbackgroundcopyfiles_skip, bits/IEnumBackgroundCopyFiles::Skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IEnumBackgroundCopyFiles.Skip
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IEnumBackgroundCopyFiles::Skip


## -description


Skips the next specified number of elements in the enumeration sequence. If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.


## -parameters




### -param celt [in]

Number of elements to skip.


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
Successfully skipped the number of requested elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped less than the number of requested elements.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa363097(v=VS.85).aspx">IEnumBackgroundCopyFiles</a>
 

 


---
UID: NF:bits3_0.IBitsPeerCacheRecord.GetFileModificationTime
title: IBitsPeerCacheRecord::GetFileModificationTime
author: windows-sdk-content
description: Gets the date and time that the file was last modified on the server.
old-location: bits\ibitspeercacherecord_getfilemodificationtime.htm
tech.root: Bits
ms.assetid: fe24b090-7dfd-4cbe-bb5d-ff3fd01723df
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetFileModificationTime, GetFileModificationTime method [BITS], GetFileModificationTime method [BITS],IBitsPeerCacheRecord interface, IBitsPeerCacheRecord interface [BITS],GetFileModificationTime method, IBitsPeerCacheRecord.GetFileModificationTime, IBitsPeerCacheRecord::GetFileModificationTime, bits.ibitspeercacherecord_getfilemodificationtime, bits3_0/IBitsPeerCacheRecord::GetFileModificationTime
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
 - IBitsPeerCacheRecord.GetFileModificationTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeerCacheRecord::GetFileModificationTime


## -description


Gets the date and time that the file was last modified on the server.


## -parameters




### -param pVal

TBD




#### - pModificationTime [out]

Date and time that the file was last modified on the server. The time is specified as 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>.


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




<a href="https://msdn.microsoft.com/en-us/library/Aa964291(v=VS.85).aspx">IBitsPeerCacheRecord</a>
 

 


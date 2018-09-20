---
UID: NF:bits3_0.IBitsPeerCacheRecord.GetLastAccessTime
title: IBitsPeerCacheRecord::GetLastAccessTime
author: windows-sdk-content
description: Gets the date and time that the file was last accessed.
old-location: bits\ibitspeercacherecord_getlastaccesstime.htm
tech.root: Bits
ms.assetid: f4443db2-3d4f-497f-b2e3-d969d8271d6f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetLastAccessTime, GetLastAccessTime method [BITS], GetLastAccessTime method [BITS],IBitsPeerCacheRecord interface, IBitsPeerCacheRecord interface [BITS],GetLastAccessTime method, IBitsPeerCacheRecord.GetLastAccessTime, IBitsPeerCacheRecord::GetLastAccessTime, bits.ibitspeercacherecord_getlastaccesstime, bits3_0/IBitsPeerCacheRecord::GetLastAccessTime
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
 - IBitsPeerCacheRecord.GetLastAccessTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeerCacheRecord::GetLastAccessTime


## -description


Gets the date and time that the file was last accessed.


## -parameters




### -param pVal

TBD




#### - pAccessTime [out]

Date and time that the file was last accessed. The time is specified as 
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




<a href="https://msdn.microsoft.com/61db33de-a38c-4c52-9f1b-66d46f25c297">IBitsPeerCacheRecord</a>
 

 


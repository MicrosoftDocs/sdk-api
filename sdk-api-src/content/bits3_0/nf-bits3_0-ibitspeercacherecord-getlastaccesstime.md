---
UID: NF:bits3_0.IBitsPeerCacheRecord.GetLastAccessTime
title: IBitsPeerCacheRecord::GetLastAccessTime
author: windows-sdk-content
description: Gets the date and time that the file was last accessed.
old-location: bits\ibitspeercacherecord_getlastaccesstime.htm
old-project: bits
ms.assetid: f4443db2-3d4f-497f-b2e3-d969d8271d6f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetLastAccessTime, GetLastAccessTime method [BITS], GetLastAccessTime method [BITS],IBitsPeerCacheRecord interface, IBitsPeerCacheRecord interface [BITS],GetLastAccessTime method, IBitsPeerCacheRecord.GetLastAccessTime, IBitsPeerCacheRecord::GetLastAccessTime, bits.ibitspeercacherecord_getlastaccesstime, bits3_0/IBitsPeerCacheRecord::GetLastAccessTime
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
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
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBitsPeerCacheRecord::GetLastAccessTime


## -description


Gets the date and time that the file was last accessed.


## -parameters




### -param pVal






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
 

 


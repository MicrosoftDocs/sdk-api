---
UID: NF:bits3_0.IBitsPeerCacheRecord.GetFileModificationTime
title: IBitsPeerCacheRecord::GetFileModificationTime (bits3_0.h)
author: windows-sdk-content
description: Gets the date and time that the file was last modified on the server.
old-location: bits\ibitspeercacherecord_getfilemodificationtime.htm
tech.root: Bits
ms.assetid: fe24b090-7dfd-4cbe-bb5d-ff3fd01723df
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFileModificationTime, GetFileModificationTime method [BITS], GetFileModificationTime method [BITS],IBitsPeerCacheRecord interface, IBitsPeerCacheRecord interface [BITS],GetFileModificationTime method, IBitsPeerCacheRecord.GetFileModificationTime, IBitsPeerCacheRecord::GetFileModificationTime, bits.ibitspeercacherecord_getfilemodificationtime, bits3_0/IBitsPeerCacheRecord::GetFileModificationTime
ms.topic: method
f1_keywords: 
 - "bits3_0/IBitsPeerCacheRecord.GetFileModificationTime"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBitsPeerCacheRecord::GetFileModificationTime


## -description


Gets the date and time that the file was last modified on the server.


## -parameters




### -param pVal [out]

Date and time that the file was last modified on the server. The time is specified as 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacherecord">IBitsPeerCacheRecord</a>
 

 


---
UID: NF:bits3_0.IBitsPeerCacheRecord.IsFileValidated
title: IBitsPeerCacheRecord::IsFileValidated
author: windows-sdk-content
description: Determines whether the file has been validated.
old-location: bits\ibitspeercacherecord_isfilevalidated.htm
old-project: bits
ms.assetid: f492f009-bef7-412e-8626-ae84cd5ce03f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IBitsPeerCacheRecord interface [BITS],IsFileValidated method, IBitsPeerCacheRecord.IsFileValidated, IBitsPeerCacheRecord::IsFileValidated, IsFileValidated, IsFileValidated method [BITS], IsFileValidated method [BITS],IBitsPeerCacheRecord interface, bits.ibitspeercacherecord_isfilevalidated, bits3_0/IBitsPeerCacheRecord::IsFileValidated
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.redist: 
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
 - IBitsPeerCacheRecord.IsFileValidated
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBitsPeerCacheRecord::IsFileValidated


## -description


Determines whether the file has been validated.


## -parameters






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
File has been validated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
File has not been validated.

</td>
</tr>
</table>
 




## -remarks



The file is available to serve after you validate the file. To validate the file, call the <a href="https://msdn.microsoft.com/en-us/library/Aa362955(v=VS.85).aspx">IBackgroundCopyFile3::SetValidationState</a> method. The file is implicitly validated if the application calls <a href="https://msdn.microsoft.com/en-us/library/Aa363021(v=VS.85).aspx">IBackgroundCopyJob::Complete</a> without calling <b>SetValidationState</b>. To remove the file from the cache after validation, see <a href="https://msdn.microsoft.com/en-us/library/Aa964276(v=VS.85).aspx">IBitsPeerCacheAdministration::DeleteUrl</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa964275(v=VS.85).aspx">IBitsPeerCacheAdministration::DeleteRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa964291(v=VS.85).aspx">IBitsPeerCacheRecord</a>
 

 


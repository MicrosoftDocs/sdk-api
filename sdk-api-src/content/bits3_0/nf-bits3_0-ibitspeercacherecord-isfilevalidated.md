---
UID: NF:bits3_0.IBitsPeerCacheRecord.IsFileValidated
title: IBitsPeerCacheRecord::IsFileValidated method
author: windows-driver-content
description: Determines whether the file has been validated.
old-location: bits\ibitspeercacherecord_isfilevalidated.htm
old-project: Bits
ms.assetid: f492f009-bef7-412e-8626-ae84cd5ce03f
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: IBitsPeerCacheRecord, IBitsPeerCacheRecord interface [BITS], IsFileValidated method, IBitsPeerCacheRecord::IsFileValidated, IsFileValidated method [BITS], IsFileValidated method [BITS], IBitsPeerCacheRecord interface, IsFileValidated,IBitsPeerCacheRecord.IsFileValidated, bits.ibitspeercacherecord_isfilevalidated, bits3_0/IBitsPeerCacheRecord::IsFileValidated
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
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bits.lib
-	Bits.dll
api_name:
-	IBitsPeerCacheRecord.IsFileValidated
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBitsPeerCacheRecord::IsFileValidated method


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



The file is available to serve after you validate the file. To validate the file, call the <a href="https://msdn.microsoft.com/c032ce32-07a4-4ab2-ae57-f9d526d1371a">IBackgroundCopyFile3::SetValidationState</a> method. The file is implicitly validated if the application calls <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> without calling <b>SetValidationState</b>. To remove the file from the cache after validation, see <a href="https://msdn.microsoft.com/d4849830-62fa-4bf4-bfad-59bcdbf1a10e">IBitsPeerCacheAdministration::DeleteUrl</a> and <a href="https://msdn.microsoft.com/c86199c3-9fe7-4d8f-8b33-b12b65b94e54">IBitsPeerCacheAdministration::DeleteRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/61db33de-a38c-4c52-9f1b-66d46f25c297">IBitsPeerCacheRecord</a>
 

 


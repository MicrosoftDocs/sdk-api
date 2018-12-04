---
UID: NF:bits3_0.IBitsPeerCacheAdministration.DeleteRecord
title: IBitsPeerCacheAdministration::DeleteRecord
author: windows-sdk-content
description: Deletes a record and file from the cache. This method uses the record's identifier to identify the record to delete.
old-location: bits\ibitspeercacheadministration_deleterecord.htm
tech.root: bits
ms.assetid: c86199c3-9fe7-4d8f-8b33-b12b65b94e54
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DeleteRecord, DeleteRecord method [BITS], DeleteRecord method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],DeleteRecord method, IBitsPeerCacheAdministration.DeleteRecord, IBitsPeerCacheAdministration::DeleteRecord, bits.ibitspeercacheadministration_deleterecord, bits3_0/IBitsPeerCacheAdministration::DeleteRecord
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
 - IBitsPeerCacheAdministration.DeleteRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeerCacheAdministration::DeleteRecord


## -description


Deletes a record and file from the cache. This method uses the record's identifier to identify the record to delete.


## -parameters




### -param id [in]

Identifier of the record to delete from the cache. The <a href="https://msdn.microsoft.com/a1894ab3-0b3f-492b-8ed7-51f3b4ee1eaa">IBitsPeerCacheRecord::GetId</a> method returns the identifier.


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
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_BUSYCACHERECORD</b></dt>
</dl>
</td>
<td width="60%">
The cache record is in use and cannot be changed or deleted.  Try again after a few seconds.

</td>
</tr>
</table>
 




## -remarks



The cache record is not removed until all current activity with the cache record is complete.




## -see-also




<a href="https://msdn.microsoft.com/5fa30b4e-f13c-4341-af65-a2e3d2703b96">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/d4849830-62fa-4bf4-bfad-59bcdbf1a10e">IBitsPeerCacheAdministration::DeleteUrl</a>



<a href="https://msdn.microsoft.com/7dd32e9c-bf4e-4dbf-aa9f-9ffbf98d3f1c">IBitsPeerCacheAdministration::GetRecord</a>
 

 


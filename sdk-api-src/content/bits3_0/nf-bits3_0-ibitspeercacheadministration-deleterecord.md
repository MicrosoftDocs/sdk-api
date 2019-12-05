---
UID: NF:bits3_0.IBitsPeerCacheAdministration.DeleteRecord
title: IBitsPeerCacheAdministration::DeleteRecord (bits3_0.h)
description: Deletes a record and file from the cache. This method uses the record's identifier to identify the record to delete.
old-location: bits\ibitspeercacheadministration_deleterecord.htm
tech.root: Bits
ms.assetid: c86199c3-9fe7-4d8f-8b33-b12b65b94e54
ms.date: 12/05/2018
ms.keywords: DeleteRecord, DeleteRecord method [BITS], DeleteRecord method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],DeleteRecord method, IBitsPeerCacheAdministration.DeleteRecord, IBitsPeerCacheAdministration::DeleteRecord, bits.ibitspeercacheadministration_deleterecord, bits3_0/IBitsPeerCacheAdministration::DeleteRecord
ms.topic: method
f1_keywords:
- bits3_0/IBitsPeerCacheAdministration.DeleteRecord
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
- IBitsPeerCacheAdministration.DeleteRecord
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBitsPeerCacheAdministration::DeleteRecord


## -description


Deletes a record and file from the cache. This method uses the record's identifier to identify the record to delete.


## -parameters




### -param id [in]

Identifier of the record to delete from the cache. The <a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacherecord-getid">IBitsPeerCacheRecord::GetId</a> method returns the identifier.


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




<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-deleteurl">IBitsPeerCacheAdministration::DeleteUrl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-getrecord">IBitsPeerCacheAdministration::GetRecord</a>
 

 


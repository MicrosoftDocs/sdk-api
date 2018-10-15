---
UID: NF:bits3_0.IBitsPeerCacheAdministration.ClearRecords
title: IBitsPeerCacheAdministration::ClearRecords
author: windows-sdk-content
description: Removes all the records and files from the cache.
old-location: bits\ibitspeercacheadministration_clearrecords.htm
tech.root: Bits
ms.assetid: 96e18c5d-6c76-4953-8e8e-3e98943478d8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ClearRecords, ClearRecords method [BITS], ClearRecords method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],ClearRecords method, IBitsPeerCacheAdministration.ClearRecords, IBitsPeerCacheAdministration::ClearRecords, bits.ibitspeercacheadministration_clearrecords, bits3_0/IBitsPeerCacheAdministration::ClearRecords
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
 - IBitsPeerCacheAdministration.ClearRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeerCacheAdministration::ClearRecords


## -description


Removes all the records and files from the cache.


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
Success

</td>
</tr>
</table>
 




## -remarks



The cache is not cleared until all current cache activity is complete.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa964272(v=VS.85).aspx">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964275(v=VS.85).aspx">IBitsPeerCacheAdministration::DeleteRecord</a>
 

 


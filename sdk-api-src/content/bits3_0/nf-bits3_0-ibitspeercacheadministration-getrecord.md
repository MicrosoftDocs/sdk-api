---
UID: NF:bits3_0.IBitsPeerCacheAdministration.GetRecord
title: IBitsPeerCacheAdministration::GetRecord
author: windows-sdk-content
description: Gets a record from the cache.
old-location: bits\ibitspeercacheadministration_getrecord.htm
tech.root: Bits
ms.assetid: 7dd32e9c-bf4e-4dbf-aa9f-9ffbf98d3f1c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRecord, GetRecord method [BITS], GetRecord method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],GetRecord method, IBitsPeerCacheAdministration.GetRecord, IBitsPeerCacheAdministration::GetRecord, bits.ibitspeercacheadministration_getrecord, bits3_0/IBitsPeerCacheAdministration::GetRecord
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
 - IBitsPeerCacheAdministration.GetRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeerCacheAdministration::GetRecord


## -description


Gets a record from the cache.


## -parameters




### -param id [in]

Identifier of the record to get from the cache. The <a href="https://msdn.microsoft.com/en-us/library/Aa964295(v=VS.85).aspx">IBitsPeerCacheRecord::GetId</a> method returns the identifier.


### -param ppRecord [out]

An <a href="https://msdn.microsoft.com/en-us/library/Aa964291(v=VS.85).aspx">IBitsPeerCacheRecord</a> interface of the cache record. Release <i>ppRecord</i> when done.


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




<a href="https://msdn.microsoft.com/en-us/library/Aa964272(v=VS.85).aspx">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964275(v=VS.85).aspx">IBitsPeerCacheAdministration::DeleteRecord</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964279(v=VS.85).aspx">IBitsPeerCacheAdministration::EnumRecords</a>
 

 


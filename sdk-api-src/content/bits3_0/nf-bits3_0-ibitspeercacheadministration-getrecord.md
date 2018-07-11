---
UID: NF:bits3_0.IBitsPeerCacheAdministration.GetRecord
title: IBitsPeerCacheAdministration::GetRecord
author: windows-sdk-content
description: Gets a record from the cache.
old-location: bits\ibitspeercacheadministration_getrecord.htm
old-project: bits
ms.assetid: 7dd32e9c-bf4e-4dbf-aa9f-9ffbf98d3f1c
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetRecord, GetRecord method [BITS], GetRecord method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],GetRecord method, IBitsPeerCacheAdministration.GetRecord, IBitsPeerCacheAdministration::GetRecord, bits.ibitspeercacheadministration_getrecord, bits3_0/IBitsPeerCacheAdministration::GetRecord
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
 - IBitsPeerCacheAdministration.GetRecord
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBitsPeerCacheAdministration::GetRecord


## -description


Gets a record from the cache.


## -parameters




### -param id [in]

Identifier of the record to get from the cache. The <a href="https://msdn.microsoft.com/a1894ab3-0b3f-492b-8ed7-51f3b4ee1eaa">IBitsPeerCacheRecord::GetId</a> method returns the identifier.


### -param ppRecord [out]

An <a href="https://msdn.microsoft.com/61db33de-a38c-4c52-9f1b-66d46f25c297">IBitsPeerCacheRecord</a> interface of the cache record. Release <i>ppRecord</i> when done.


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




<a href="https://msdn.microsoft.com/5fa30b4e-f13c-4341-af65-a2e3d2703b96">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/c86199c3-9fe7-4d8f-8b33-b12b65b94e54">IBitsPeerCacheAdministration::DeleteRecord</a>



<a href="https://msdn.microsoft.com/b471cee0-0ad0-4488-9819-e524e50dbc76">IBitsPeerCacheAdministration::EnumRecords</a>
 

 


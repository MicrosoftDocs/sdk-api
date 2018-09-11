---
UID: NF:dskquota.IEnumDiskQuotaUsers.Clone
title: IEnumDiskQuotaUsers::Clone
author: windows-sdk-content
description: Creates another enumerator of user quota entries that contains the same enumeration state as the current one.
old-location: fs\ienumdiskquotausers_clone.htm
tech.root: fileio
ms.assetid: 1c01b2d5-5419-4694-819f-fe6ef6e1636b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Clone, Clone method [Files], Clone method [Files],IEnumDiskQuotaUsers interface, IEnumDiskQuotaUsers interface [Files],Clone method, IEnumDiskQuotaUsers.Clone, IEnumDiskQuotaUsers::Clone, _win32_ienumdiskquotausers_clone, base.ienumdiskquotausers_clone, dskquota/IEnumDiskQuotaUsers::Clone, fs.ienumdiskquotausers_clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dskquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Dskquota.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IEnumDiskQuotaUsers.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDiskQuotaUsers::Clone


## -description


Creates another enumerator of user quota entries that contains the same enumeration state as the current one. Using this method, a client can record a particular point in the enumeration sequence, and then return to that point at a later time. The new enumerator supports the same interface as the original one.


## -parameters




### -param ppEnum [out]

A pointer to the 
<a href="https://msdn.microsoft.com/f5916b17-66ed-46d4-87f1-5ee2ef57c1a1">IEnumDiskQuotaUsers</a> interface pointer. If the method is unsuccessful, the value of this variable is undefined.


## -returns



This method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnum</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected exception occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>



<a href="https://msdn.microsoft.com/f5916b17-66ed-46d4-87f1-5ee2ef57c1a1">IEnumDiskQuotaUsers</a>
 

 


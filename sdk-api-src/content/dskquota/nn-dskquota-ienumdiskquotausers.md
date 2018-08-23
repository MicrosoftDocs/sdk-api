---
UID: NN:dskquota.IEnumDiskQuotaUsers
title: IEnumDiskQuotaUsers
author: windows-sdk-content
description: Enumerates user quota entries on the volume.
old-location: fs\ienumdiskquotausers.htm
old-project: fileio
ms.assetid: f5916b17-66ed-46d4-87f1-5ee2ef57c1a1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumDiskQuotaUsers, IEnumDiskQuotaUsers interface [Files], IEnumDiskQuotaUsers interface [Files],described, _win32_ienumdiskquotausers, base.ienumdiskquotausers, dskquota/IEnumDiskQuotaUsers, fs.ienumdiskquotausers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dskquota.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IEnumDiskQuotaUsers
product: Windows
targetos: Windows
req.lib: 
req.dll: Dskquota.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnumDiskQuotaUsers interface


## -description


Enumerates user quota entries on the volume. This interface is instantiated by using the 
<a href="https://msdn.microsoft.com/a29e1955-80e2-442d-9565-c885006be565">IDiskQuotaControl::CreateEnumUsers</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDiskQuotaUsers</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumDiskQuotaUsers</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumDiskQuotaUsers</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c01b2d5-5419-4694-819f-fe6ef6e1636b">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/498e7c21-b18a-4d43-bbe6-9f20c2e26221">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>cUsers</i> items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c19d4cbe-e83f-4a2d-9eb1-77f32717f69e">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b37462aa-cd1c-4986-ad23-f9523c962d19">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>
 

 


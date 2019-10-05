---
UID: NN:dskquota.IEnumDiskQuotaUsers
title: IEnumDiskQuotaUsers (dskquota.h)
author: windows-sdk-content
description: Enumerates user quota entries on the volume.
old-location: fs\ienumdiskquotausers.htm
tech.root: FileIO
ms.assetid: f5916b17-66ed-46d4-87f1-5ee2ef57c1a1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumDiskQuotaUsers, IEnumDiskQuotaUsers interface [Files], IEnumDiskQuotaUsers interface [Files],described, _win32_ienumdiskquotausers, base.ienumdiskquotausers, dskquota/IEnumDiskQuotaUsers, fs.ienumdiskquotausers
ms.topic: interface
f1_keywords: 
 - "dskquota/IEnumDiskQuotaUsers"
dev_langs:
 - c++
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
 - IEnumDiskQuotaUsers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumDiskQuotaUsers interface


## -description


Enumerates user quota entries on the volume. This interface is instantiated by using the 
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-createenumusers">IDiskQuotaControl::CreateEnumUsers</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDiskQuotaUsers</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumDiskQuotaUsers</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-ienumdiskquotausers-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-ienumdiskquotausers-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>cUsers</i> items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-ienumdiskquotausers-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-ienumdiskquotausers-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>
 

 


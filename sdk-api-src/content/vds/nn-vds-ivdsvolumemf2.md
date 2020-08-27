---
UID: NN:vds.IVdsVolumeMF2
title: IVdsVolumeMF2 (vds.h)
description: Provides methods to perform additional file system management operations on the volume object.
helpviewer_keywords: ["IVdsVolumeMF2","IVdsVolumeMF2 interface","IVdsVolumeMF2 interface","described","base.ivdsvolumemf2","vds/IVdsVolumeMF2"]
old-location: base\ivdsvolumemf2.htm
tech.root: base
ms.assetid: 3219233e-7141-472a-8cb9-207222a4e775
ms.date: 12/05/2018
ms.keywords: IVdsVolumeMF2, IVdsVolumeMF2 interface, IVdsVolumeMF2 interface,described, base.ivdsvolumemf2, vds/IVdsVolumeMF2
f1_keywords:
- vds/IVdsVolumeMF2
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsVolumeMF2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVolumeMF2 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

 Provides methods to perform additional file system management operations on the volume object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumeMF2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsVolumeMF2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolumeMF2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf2-formatex">FormatEx</a>
</td>
<td align="left" width="63%">
Formats a file system on a volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf2-getfilesystemtypename">GetFileSystemTypeName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file system on a volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf2-queryfilesystemformatsupport">QueryFileSystemFormatSupport</a>
</td>
<td align="left" width="63%">
Retrieves the properties of the file systems that are supported for formatting a volume.

</td>
</tr>
</table> 


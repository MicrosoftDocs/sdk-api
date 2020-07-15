---
UID: NN:vds.IVdsServiceUninstallDisk
title: IVdsServiceUninstallDisk (vds.h)
description: Provides methods to uninstall basic and dynamic disks.
helpviewer_keywords: ["IVdsServiceUninstallDisk","IVdsServiceUninstallDisk interface","IVdsServiceUninstallDisk interface","described","base.ivdsserviceuninstalldisk","vds/IVdsServiceUninstallDisk"]
old-location: base\ivdsserviceuninstalldisk.htm
tech.root: VDS
ms.assetid: 2d111105-9970-40a3-bb8d-a92d38985fd9
ms.date: 12/05/2018
ms.keywords: IVdsServiceUninstallDisk, IVdsServiceUninstallDisk interface, IVdsServiceUninstallDisk interface,described, base.ivdsserviceuninstalldisk, vds/IVdsServiceUninstallDisk
f1_keywords:
- vds/IVdsServiceUninstallDisk
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
- IVdsServiceUninstallDisk
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsServiceUninstallDisk interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to uninstall basic and dynamic disks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsServiceUninstallDisk</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsServiceUninstallDisk</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsServiceUninstallDisk</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceuninstalldisk-getdiskidfromluninfo">GetDiskIdFromLunInfo</a>
</td>
<td align="left" width="63%">
Retrieves the VDS object ID for the disk that corresponds to a specified LUN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceuninstalldisk-uninstalldisks">UninstallDisks</a>
</td>
<td align="left" width="63%">
Uninstalls a set of disks.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/startup-and-service-objects">Service Object</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 


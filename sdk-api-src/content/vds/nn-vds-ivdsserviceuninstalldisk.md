---
UID: NN:vds.IVdsServiceUninstallDisk
title: IVdsServiceUninstallDisk (vds.h)
author: windows-sdk-content
description: Provides methods to uninstall basic and dynamic disks.
old-location: base\ivdsserviceuninstalldisk.htm
tech.root: VDS
ms.assetid: 2d111105-9970-40a3-bb8d-a92d38985fd9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsServiceUninstallDisk, IVdsServiceUninstallDisk interface, IVdsServiceUninstallDisk interface,described, base.ivdsserviceuninstalldisk, vds/IVdsServiceUninstallDisk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsServiceUninstallDisk interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to uninstall basic and dynamic disks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsServiceUninstallDisk</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsServiceUninstallDisk</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0059bb30-2799-4a41-8a5c-bae3aa2bcfc4">GetDiskIdFromLunInfo</a>
</td>
<td align="left" width="63%">
Retrieves the VDS object ID for the disk that corresponds to a specified LUN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65c5444f-7e97-4746-9d74-561dc435212d">UninstallDisks</a>
</td>
<td align="left" width="63%">
Uninstalls a set of disks.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383123(v=VS.85).aspx">Service Object</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 


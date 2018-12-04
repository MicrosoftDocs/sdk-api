---
UID: NN:vds.IVdsVolumeMF3
title: IVdsVolumeMF3
author: windows-sdk-content
description: Provides methods to perform additional file system management operations on the volume object.
old-location: base\ivdsvolumemf3.htm
tech.root: vds
ms.assetid: 46b8ff26-c00b-45ef-ac30-0aa82786bf9b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IVdsVolumeMF3, IVdsVolumeMF3 interface, IVdsVolumeMF3 interface,described, base.ivdsvolumemf3, vds/IVdsVolumeMF3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsVolumeMF3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVolumeMF3 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

 Provides methods to perform additional file system management operations on the volume object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumeMF3</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsVolumeMF3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolumeMF3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9ef47e2-552c-4630-9f63-84f00bd93fa6">FormatEx2</a>
</td>
<td align="left" width="63%">
Formats a file system volume on a partition. This method is identical to the <a href="https://msdn.microsoft.com/c1d08018-4e9b-466a-b8dd-074b2ce0c8fe">IVdsVolumeMF2::FormatEx</a> method, except that formatting options are specified by using the <i>Options</i> parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7f699c6-6f1c-445d-80b4-3576102d5b5f">OfflineVolume</a>
</td>
<td align="left" width="63%">
Takes the volume offline by using the <a href="https://msdn.microsoft.com/7c9b97eb-c167-41cd-b235-7a9d7830915e">IOCTL_VOLUME_OFFLINE</a> control code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08311403-23a9-4191-9720-3cec805de825">QueryVolumeGuidPathnames</a>
</td>
<td align="left" width="63%">
Returns a list of volume GUID paths for the current volume.

</td>
</tr>
</table> 


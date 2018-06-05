---
UID: NN:vds.IVdsVolumeMF2
title: IVdsVolumeMF2
author: windows-sdk-content
description: Provides methods to perform additional file system management operations on the volume object.
old-location: base\ivdsvolumemf2.htm
old-project: VDS
ms.assetid: 3219233e-7141-472a-8cb9-207222a4e775
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsVolumeMF2, IVdsVolumeMF2 interface, IVdsVolumeMF2 interface,described, base.ivdsvolumemf2, vds/IVdsVolumeMF2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsVolumeMF2
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolumeMF2 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

 Provides methods to perform additional file system management operations on the volume object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumeMF2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsVolumeMF2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c1d08018-4e9b-466a-b8dd-074b2ce0c8fe">FormatEx</a>
</td>
<td align="left" width="63%">
Formats a file system on a volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9e8627b-0531-4dcb-9818-7560372aa4b0">GetFileSystemTypeName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file system on a volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/770a92fb-9e70-4db0-a782-b9064daef4ef">QueryFileSystemFormatSupport</a>
</td>
<td align="left" width="63%">
Retrieves the properties of the file systems that are supported for formatting a volume.

</td>
</tr>
</table> 


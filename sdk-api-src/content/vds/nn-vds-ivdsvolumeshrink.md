---
UID: NN:vds.IVdsVolumeShrink
title: IVdsVolumeShrink
author: windows-sdk-content
description: Provides methods to support volume shrinking.
old-location: base\ivdsvolumeshrink.htm
old-project: VDS
ms.assetid: 08c354a6-5cc0-405c-91cf-dca55b87b49a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVdsVolumeShrink, IVdsVolumeShrink interface, IVdsVolumeShrink interface,described, base.ivdsvolumeshrink, vds/IVdsVolumeShrink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vds.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVolumeShrink
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolumeShrink interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to support volume shrinking.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumeShrink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsVolumeShrink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolumeShrink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/416ceb78-50fb-4976-8814-3981b594ebec">QueryMaxReclaimableBytes</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of bytes that can be reclaimed from the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6d91cb0-b9a4-4a5f-94bc-824b1691bcd7">Shrink</a>
</td>
<td align="left" width="63%">
Shrinks the volume and all plexes and returns the released extents.

</td>
</tr>
</table> 


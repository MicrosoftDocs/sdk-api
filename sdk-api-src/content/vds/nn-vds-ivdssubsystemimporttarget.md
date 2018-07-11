---
UID: NN:vds.IVdsSubSystemImportTarget
title: IVdsSubSystemImportTarget
author: windows-sdk-content
description: Provides methods to query and configure the default VSS import target for the subsystem.
old-location: base\ivdssubsystemimporttarget.htm
old-project: vds
ms.assetid: c9e2f353-d5d4-47a2-8398-5cbd9d499fb7
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: IVdsSubSystemImportTarget, IVdsSubSystemImportTarget interface [VDS], IVdsSubSystemImportTarget interface [VDS],described, base.ivdssubsystemimporttarget, vds/IVdsSubSystemImportTarget
ms.prod: windows
ms.technology: windows-sdk
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
 - IVdsSubSystemImportTarget
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsSubSystemImportTarget interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to query and configure the default VSS import target for the 
   subsystem.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSubSystemImportTarget</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsSubSystemImportTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSubSystemImportTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fff1400-61d9-494f-857d-53626b80c2d2">GetImportTarget</a>
</td>
<td align="left" width="63%">
Returns the VSS import target for the computer for this subsystem.</p> (Inherited from <b>IVdsSubSystemImportTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96770760-a9af-46be-8e63-be8a86ec81ab">SetImportTarget</a>
</td>
<td align="left" width="63%">
Sets the VSS import target for the computer for this subsystem.</p> (Inherited from <b>IVdsSubSystemImportTarget</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 


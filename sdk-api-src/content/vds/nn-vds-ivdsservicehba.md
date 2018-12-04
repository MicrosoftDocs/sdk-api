---
UID: NN:vds.IVdsServiceHba
title: IVdsServiceHba
author: windows-sdk-content
description: Provides a method to query HBA ports on the local system.
old-location: base\ivdsservicehba.htm
tech.root: vds
ms.assetid: 0f3375fa-fc17-4808-ac29-a772a9c13850
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IVdsServiceHba, IVdsServiceHba interface [VDS], IVdsServiceHba interface [VDS],described, base.ivdsservicehba, vds/IVdsServiceHba
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVdsServiceHba
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsServiceHba interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method to 
   query HBA ports on the local system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsServiceHba</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsServiceHba</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsServiceHba</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f81e5e9-5563-4435-8ecb-82f2c385c3dc">QueryHbaPorts</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> enumeration object containing 
     a list of the HBA ports known to VDS on the local system.</p> (Inherited from <b>IVdsServiceHba</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 


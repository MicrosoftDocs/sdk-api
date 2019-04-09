---
UID: NN:vds.IVdsMaintenance
title: IVdsMaintenance (vds.h)
author: windows-sdk-content
description: Provides methods for performing maintenance operations on a subsystem, controller, LUN, or drive.
old-location: base\ivdsmaintenance.htm
tech.root: VDS
ms.assetid: 08c01459-151a-4dd8-bea5-412076e39a8a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsMaintenance, IVdsMaintenance interface [VDS], IVdsMaintenance interface [VDS],described, base.ivdsmaintenance, vds/IVdsMaintenance, vdshwprv/IVdsMaintenance
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IVdsMaintenance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsMaintenance interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for performing maintenance operations on a subsystem, controller, LUN, or drive.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsMaintenance</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsMaintenance</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsMaintenance</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/057424eb-c491-4295-b2a7-cf983902c667">PulseMaintenance</a>
</td>
<td align="left" width="63%">
Performs the specified operation a specified number of times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d2e1022-ae79-4f71-a488-2c86b43b2a7f">StartMaintenance</a>
</td>
<td align="left" width="63%">
Starts a maintenance operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/542f84d7-eb97-4738-b7c0-1c95bc5e063c">StopMaintenance</a>
</td>
<td align="left" width="63%">
Stops a maintenance operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 


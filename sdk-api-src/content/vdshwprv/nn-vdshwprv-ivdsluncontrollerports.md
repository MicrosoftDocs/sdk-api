---
UID: NN:vdshwprv.IVdsLunControllerPorts
title: IVdsLunControllerPorts
author: windows-sdk-content
description: Provides methods for performing controller port configuration operations on a LUN.
old-location: base\ivdsluncontrollerports.htm
tech.root: VDS
ms.assetid: 81e48874-8bc2-4b82-bcf8-ce87f99ca3ad
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsLunControllerPorts, IVdsLunControllerPorts interface [VDS], IVdsLunControllerPorts interface [VDS],described, base.ivdsluncontrollerports, vds/IVdsLunControllerPorts, vdshwprv/IVdsLunControllerPorts
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vdshwprv.h
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
 - IVdsLunControllerPorts
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsLunControllerPorts interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides 
   methods for performing controller port configuration operations on a LUN.
  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLunControllerPorts</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsLunControllerPorts</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLunControllerPorts</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b889cb7-92e4-4c18-b9b9-768865895595">AssociateControllerPorts</a>
</td>
<td align="left" width="63%">
Sets the subsystem controller ports to active or inactive with respect to the LUN. This method replaces 
     <a href="https://msdn.microsoft.com/2c3dc668-1745-49f4-9cd1-3bf0b322d0b2">IVdsLun::AssociateControllers</a>.
 (Inherited from <b>IVdsLunControllerPorts</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a6f34c6-f333-4abf-ad37-b7756b125045">QueryActiveControllerPorts</a>
</td>
<td align="left" width="63%">
Returns an enumeration of currently active controller ports.</p> (Inherited from <b>IVdsLunControllerPorts</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 


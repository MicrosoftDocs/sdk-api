---
UID: NN:vdshwprv.IVdsControllerControllerPort
title: IVdsControllerControllerPort
author: windows-sdk-content
description: Provides a method to enumerate controller ports for a class implementing the IVdsController interface. This is needed to support MPIO.
old-location: base\ivdscontrollercontrollerport.htm
old-project: vds
ms.assetid: 15b09f97-c729-4687-a62c-dac57661f8c0
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsControllerControllerPort, IVdsControllerControllerPort interface [VDS], IVdsControllerControllerPort interface [VDS],described, base.ivdscontrollercontrollerport, vds/IVdsControllerControllerPort, vdshwprv/IVdsControllerControllerPort
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vdshwprv.h
req.include-header: 
req.redist: 
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
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsControllerControllerPort
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsControllerControllerPort interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method to enumerate controller ports for a class implementing the 
   <a href="https://msdn.microsoft.com/cc30a78a-78a4-49c2-a97d-228400da46a9">IVdsController</a> interface. This is needed to support 
   MPIO.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsControllerControllerPort</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsControllerControllerPort</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsControllerControllerPort</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/676d0ae9-7d9e-4dc3-93c2-56c96a05ac0a">QueryControllerPorts</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> object that enumerates the 
     ports of the controller.</p> (Inherited from <b>IVdsControllerControllerPort</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8">Controller Object</a>



<a href="https://msdn.microsoft.com/cc30a78a-78a4-49c2-a97d-228400da46a9">IVdsController</a>



<a href="https://msdn.microsoft.com/676d0ae9-7d9e-4dc3-93c2-56c96a05ac0a">QueryControllerPorts</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 


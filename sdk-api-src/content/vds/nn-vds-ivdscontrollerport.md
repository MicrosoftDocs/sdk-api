---
UID: NN:vds.IVdsControllerPort
title: IVdsControllerPort
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on a controller port.
old-location: base\ivdscontrollerport.htm
tech.root: VDS
ms.assetid: a0ceaf1d-b839-4cf7-b64e-9100f3cf23ef
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsControllerPort, IVdsControllerPort interface [VDS], IVdsControllerPort interface [VDS],described, base.ivdscontrollerport, vds/IVdsControllerPort, vdshwprv/IVdsControllerPort
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
 - IVdsControllerPort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsControllerPort interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for performing 
   query and configuration operations on a controller port.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsControllerPort</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsControllerPort</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsControllerPort</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12532ac2-96bd-4ebf-9d09-c240e7357e20">GetController</a>
</td>
<td align="left" width="63%">
Returns the controller to which the controller port belongs.</p> (Inherited from <b>IVdsControllerPort</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7540f2d3-c17c-4868-9e72-116219bab51c">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties of a controller port.</p> (Inherited from <b>IVdsControllerPort</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/062b820e-f384-4c2e-a2f7-c90748c74976">QueryAssociatedLuns</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the LUNs with which the controller port is associated—the LUNs 
     for which the controller is active. This method replaces 
     <a href="https://msdn.microsoft.com/832b8d59-6e94-4d62-a31f-4658e9f6102b">IVdsController::QueryAssociatedLuns</a>.
 (Inherited from <b>IVdsControllerPort</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e298ef9d-8abb-450b-97d3-e97d64f0e734">Reset</a>
</td>
<td align="left" width="63%">
Reinitializes the controller port.</p> (Inherited from <b>IVdsControllerPort</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1338e1e7-80c8-409d-aa54-575618fd9797">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of a controller port to the specified value.</p> (Inherited from <b>IVdsControllerPort</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cc30a78a-78a4-49c2-a97d-228400da46a9">IVdsController</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 


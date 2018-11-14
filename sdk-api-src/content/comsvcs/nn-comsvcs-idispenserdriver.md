---
UID: NN:comsvcs.IDispenserDriver
title: IDispenserDriver
author: windows-sdk-content
description: Is called by the holder of the COM+ Resource Dispenser to create, enlist, evaluate, prepare, and destroy a resource.
old-location: cos\idispenserdriver.htm
tech.root: cossdk
ms.assetid: dba9c616-031d-48a7-b3e3-eb28b95a573a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDispenserDriver, IDispenserDriver interface [COM+], IDispenserDriver interface [COM+],described, _dtc_IDispenserDriver_Interface, comsvcs/IDispenserDriver, cos.idispenserdriver
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IDispenserDriver
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDispenserDriver interface


## -description


Is called by the holder of the <a href="https://msdn.microsoft.com/34825538-85dd-4e86-a306-79cd60b3bc0b">COM+ Resource Dispenser</a> to create, enlist, evaluate, prepare, and destroy a resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDispenserDriver</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDispenserDriver</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDispenserDriver</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97b49069-3428-48da-a818-737f3bc342d0">CreateResource</a>
</td>
<td align="left" width="63%">
Creates a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94e3e340-7dde-4b7f-82a9-83cd2400bde5">DestroyResource</a>
</td>
<td align="left" width="63%">
Destroys a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c7fe9ca-8a27-4459-a95d-084d717d3a65">DestroyResourceS</a>
</td>
<td align="left" width="63%">
Destroys a resource (string resource version).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87a8b7f4-edf3-4ab5-b75a-f8fda1f4975a">EnlistResource</a>
</td>
<td align="left" width="63%">
Enlists a resource in a transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fe3ca39-e4cb-4dae-be96-ce1a2099486a">RateResource</a>
</td>
<td align="left" width="63%">
Evaluates how well a candidate resource matches.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59df0703-90ea-480c-8608-7d43039b48ba">ResetResource</a>
</td>
<td align="left" width="63%">
Prepares the resource to be put back into general or enlisted inventory.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>
 

 


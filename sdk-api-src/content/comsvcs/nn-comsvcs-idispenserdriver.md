---
UID: NN:comsvcs.IDispenserDriver
title: IDispenserDriver (comsvcs.h)
author: windows-sdk-content
description: Is called by the holder of the COM+ Resource Dispenser to create, enlist, evaluate, prepare, and destroy a resource.
old-location: cos\idispenserdriver.htm
tech.root: cossdk
ms.assetid: dba9c616-031d-48a7-b3e3-eb28b95a573a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDispenserDriver, IDispenserDriver interface [COM+], IDispenserDriver interface [COM+],described, _dtc_IDispenserDriver_Interface, comsvcs/IDispenserDriver, cos.idispenserdriver
ms.topic: interface
f1_keywords: 
 - "comsvcs/IDispenserDriver"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDispenserDriver interface


## -description


Is called by the holder of the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--resource-dispenser-service">COM+ Resource Dispenser</a> to create, enlist, evaluate, prepare, and destroy a resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDispenserDriver</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDispenserDriver</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-createresource">CreateResource</a>
</td>
<td align="left" width="63%">
Creates a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-destroyresource">DestroyResource</a>
</td>
<td align="left" width="63%">
Destroys a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-destroyresources">DestroyResourceS</a>
</td>
<td align="left" width="63%">
Destroys a resource (string resource version).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-enlistresource">EnlistResource</a>
</td>
<td align="left" width="63%">
Enlists a resource in a transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-rateresource">RateResource</a>
</td>
<td align="left" width="63%">
Evaluates how well a candidate resource matches.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-resetresource">ResetResource</a>
</td>
<td align="left" width="63%">
Prepares the resource to be put back into general or enlisted inventory.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>
 

 


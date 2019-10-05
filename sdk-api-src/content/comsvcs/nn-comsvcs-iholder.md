---
UID: NN:comsvcs.IHolder
title: IHolder (comsvcs.h)
author: windows-sdk-content
description: Allocates or frees resources for an installed Resource Dispenser.
old-location: cos\iholder.htm
tech.root: cossdk
ms.assetid: 3c852e72-2fdc-4fd0-b523-f5601154da2a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IHolder, IHolder interface [COM+], IHolder interface [COM+],described, _dtc_IHolder_Interface, comsvcs/IHolder, cos.iholder
ms.topic: interface
f1_keywords: 
 - "comsvcs/IHolder"
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
 - IHolder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHolder interface


## -description


Allocates or frees resources for an installed Resource Dispenser. The Dispenser Manager exposes a different <b>IHolder</b> interface to each installed Resource Dispenser.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHolder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IHolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iholder-allocresource">AllocResource</a>
</td>
<td align="left" width="63%">
Allocates a resource from the inventory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iholder-close">Close</a>
</td>
<td align="left" width="63%">
Closes the Holder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iholder-freeresource">FreeResource</a>
</td>
<td align="left" width="63%">
Returns a resource to the inventory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iholder-requestdestroyresource">RequestDestroyResource</a>
</td>
<td align="left" width="63%">
Deletes a resource, calling its destructor to free memory and other associated system resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iholder-trackresource">TrackResource</a>
</td>
<td align="left" width="63%">
Tracks the resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iholder-trackresources">TrackResourceS</a>
</td>
<td align="left" width="63%">
Tracks the resource (string version).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iholder-untrackresource">UntrackResource</a>
</td>
<td align="left" width="63%">
Stops tracking a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iholder-untrackresources">UnTrackResourceS</a>
</td>
<td align="left" width="63%">
Stops tracking a resource (string version).

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>
 

 


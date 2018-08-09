---
UID: NN:vdshwprv.IVdsController
title: IVdsController
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on a controller.
old-location: base\ivdscontroller.htm
old-project: vds
ms.assetid: cc30a78a-78a4-49c2-a97d-228400da46a9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsController, IVdsController interface [VDS], IVdsController interface [VDS],described, base.ivdscontroller, vds/IVdsController, vdshwprv/IVdsController
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vdshwprv.h
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
 - IVdsController
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsController interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for 
   performing query and configuration operations on a controller.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsController</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsController</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsController</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a27a887d-c254-4e50-be96-564db12a673a">FlushCache</a>
</td>
<td align="left" width="63%">
Flushes the cache of the controller to a persistent store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01972923-2a43-4a80-80f8-8dab4207bbc4">GetPortProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the specified controller port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the controller.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8635d594-b58a-4ee1-9966-1340d954da81">GetSubSystem</a>
</td>
<td align="left" width="63%">
Returns the subsystem to which the controller belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91f77390-02eb-4c5f-a5de-382df608f0df">InvalidateCache</a>
</td>
<td align="left" width="63%">
Invalidates the cache of the controller. All data in the cache is lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/832b8d59-6e94-4d62-a31f-4658e9f6102b">QueryAssociatedLuns</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the LUNs with which the controller is associated—in other words, the LUNs for which the controller is active.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Reinitializes the controller and invalidates its cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9bae451-ef47-46ad-a11e-b7b36a031a8a">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of the controller to the specified value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8">Controller Object</a>



<a href="https://msdn.microsoft.com/15b09f97-c729-4687-a62c-dac57661f8c0">IVdsControllerControllerPort</a>



<a href="https://msdn.microsoft.com/2c3dc668-1745-49f4-9cd1-3bf0b322d0b2">IVdsLun::AssociateControllers</a>



<a href="https://msdn.microsoft.com/61f32915-c616-477e-b0f0-4a7f92aca0e2">IVdsSubSystem::QueryControllers</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/b9da3920-9bae-4198-ba0d-a0755aee15e4">VDS_CONTROLLER_PROP</a>
 

 


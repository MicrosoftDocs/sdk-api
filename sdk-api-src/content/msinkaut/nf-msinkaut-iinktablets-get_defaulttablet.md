---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IInkTablets::get_DefaultTablet


## -description



Gets the default tablet within the set of available tablets.



This property is read-only.


## -parameters


## -remarks



The platform determines the default <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object in the following order:

<ul>
<li>If the system has a digitizer integrated with the display device, this integrated digitizer is considered the default tablet, even if other digitizing tablets are installed.</li>
<li>If more than one digitizing tablet is installed in the system, the first one encountered during initialization is considered the default tablet.</li>
<li>If only one digitizing tablet is installed in the system, it is considered the default tablet.</li>
<li>If no digitizing tablets are installed in the system but there are other pointing devices (such as a mouse or a touch pad) installed that generate mouse messages, those devices in aggregate are considered to be the default tablet.</li>
<li>If no digitizing tablets and no pointing devices are installed in the system, no default tablet can be returned.</li>
</ul>
<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="tablet.iinktablets">IInkTablets</a>



<a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets Collection</a>
 

 


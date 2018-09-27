---
UID: NF:msinkaut.IInkTablets.get_DefaultTablet
title: IInkTablets::get_DefaultTablet
author: windows-sdk-content
description: Gets the default tablet within the set of available tablets.
old-location: tablet\inktablets_defaulttablet.htm
tech.root: tablet
ms.assetid: 4a9713c6-91a0-4632-9c8d-58d5e1b98478
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 4a9713c6-91a0-4632-9c8d-58d5e1b98478, DefaultTablet property [Tablet PC], DefaultTablet property [Tablet PC],IInkTablets interface, IInkTablets interface [Tablet PC],DefaultTablet property, IInkTablets.DefaultTablet, IInkTablets.get_DefaultTablet, IInkTablets::DefaultTablet, IInkTablets::get_DefaultTablet, InkTablets.get_DefaultTablet, get_DefaultTablet, msinkaut/IInkTablets::DefaultTablet, msinkaut/IInkTablets::get_DefaultTablet, tablet.inktablets_defaulttablet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkTablets.DefaultTablet
 - IInkTablets.get_DefaultTablet
 - InkTablets.get_DefaultTablet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



<a href="https://msdn.microsoft.com/98052ECB-9385-45C9-A03C-3F312ADD9872">IInkTablets</a>



<a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets Collection</a>
 

 


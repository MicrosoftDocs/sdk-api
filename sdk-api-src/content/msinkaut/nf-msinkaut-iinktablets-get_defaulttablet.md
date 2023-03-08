---
UID: NF:msinkaut.IInkTablets.get_DefaultTablet
title: IInkTablets::get_DefaultTablet (msinkaut.h)
description: Gets the default tablet within the set of available tablets.
helpviewer_keywords: ["4a9713c6-91a0-4632-9c8d-58d5e1b98478","DefaultTablet property [Tablet PC]","DefaultTablet property [Tablet PC]","IInkTablets interface","IInkTablets interface [Tablet PC]","DefaultTablet property","IInkTablets.DefaultTablet","IInkTablets.get_DefaultTablet","IInkTablets::DefaultTablet","IInkTablets::get_DefaultTablet","InkTablets.get_DefaultTablet","get_DefaultTablet","msinkaut/IInkTablets::DefaultTablet","msinkaut/IInkTablets::get_DefaultTablet","tablet.inktablets_defaulttablet"]
old-location: tablet\inktablets_defaulttablet.htm
tech.root: tablet
ms.assetid: 4a9713c6-91a0-4632-9c8d-58d5e1b98478
ms.date: 12/05/2018
ms.keywords: 4a9713c6-91a0-4632-9c8d-58d5e1b98478, DefaultTablet property [Tablet PC], DefaultTablet property [Tablet PC],IInkTablets interface, IInkTablets interface [Tablet PC],DefaultTablet property, IInkTablets.DefaultTablet, IInkTablets.get_DefaultTablet, IInkTablets::DefaultTablet, IInkTablets::get_DefaultTablet, InkTablets.get_DefaultTablet, get_DefaultTablet, msinkaut/IInkTablets::DefaultTablet, msinkaut/IInkTablets::get_DefaultTablet, tablet.inktablets_defaulttablet
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkTablets::get_DefaultTablet
 - msinkaut/IInkTablets::get_DefaultTablet
dev_langs:
 - c++
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
---

# IInkTablets::get_DefaultTablet


## -description

Gets the default tablet within the set of available tablets.



This property is read-only.

## -parameters

## -remarks

The platform determines the default <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object in the following order:

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

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="../msinkaut/nn-msinkaut-iinktablets.md">IInkTablets</a>



<a href="/previous-versions/windows/desktop/legacy/ms704832(v=vs.85)">InkTablets Collection</a>

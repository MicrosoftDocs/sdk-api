---
UID: NF:msinkaut.IInkTablet.get_HardwareCapabilities
title: IInkTablet::get_HardwareCapabilities
author: windows-driver-content
description: Gets a bitmask that defines the hardware capabilities of the tablet, such as whether a cursor must be in physical contact with the tablet to report its position.
old-location: tablet\iinktablet_hardwarecapabilities.htm
old-project: tablet
ms.assetid: 886c1e7c-fec0-4294-aba1-8e0806c2d0ca
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: 886c1e7c-fec0-4294-aba1-8e0806c2d0ca, HardwareCapabilities property [Tablet PC], HardwareCapabilities property [Tablet PC],IInkTablet interface, IInkTablet interface [Tablet PC],HardwareCapabilities property, IInkTablet.HardwareCapabilities, IInkTablet.get_HardwareCapabilities, IInkTablet::HardwareCapabilities, IInkTablet::get_HardwareCapabilities, get_HardwareCapabilities, msinkaut/IInkTablet::HardwareCapabilities, msinkaut/IInkTablet::get_HardwareCapabilities, tablet.iinktablet_hardwarecapabilities
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkTablet.HardwareCapabilities
-	IInkTablet.get_HardwareCapabilities
-	IInkTablet.get_HardwareCapabilities
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkTablet::get_HardwareCapabilities


## -description



Gets a bitmask that defines the hardware capabilities of the tablet, such as whether a cursor must be in physical contact with the tablet to report its position.



This property is read-only.


## -parameters


## -remarks



For a complete list of hardware capability values that you can use, see the <a href="https://msdn.microsoft.com/ab8dfca3-df5e-40a7-9da2-d19447bc746b">TabletHardwareCapabilities</a> enumeration type.

<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: WM_ACTIVATE, WM_ACTIVATEAPP, WMNCACTIVATE, WM_PAINT; WM_SYSCOMMAND if <b>wParam</b> is set to SC_HOTKEY or SC_TASKLIST; and WM_SYSKEYDOWN (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/ab8dfca3-df5e-40a7-9da2-d19447bc746b">TabletHardwareCapabilities Enumeration</a>
 

 


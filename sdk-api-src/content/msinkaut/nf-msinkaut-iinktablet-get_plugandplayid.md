---
UID: NF:msinkaut.IInkTablet.get_PlugAndPlayId
title: IInkTablet::get_PlugAndPlayId
author: windows-sdk-content
description: Gets a string representation of the Plug and Play identifier of the IInkTablet object.
old-location: tablet\iinktablet_plugandplayid.htm
old-project: tablet
ms.assetid: 5b33bd06-fee3-41b0-b3c1-d16b43685c60
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 5b33bd06-fee3-41b0-b3c1-d16b43685c60, IInkTablet interface [Tablet PC],PlugAndPlayID property, IInkTablet.PlugAndPlayID, IInkTablet.get_PlugAndPlayID, IInkTablet.get_PlugAndPlayId, IInkTablet::PlugAndPlayID, IInkTablet::get_PlugAndPlayID, IInkTablet::get_PlugAndPlayId, PlugAndPlayID property [Tablet PC], PlugAndPlayID property [Tablet PC],IInkTablet interface, get_PlugAndPlayId, msinkaut/IInkTablet::PlugAndPlayID, msinkaut/IInkTablet::get_PlugAndPlayID, tablet.iinktablet_plugandplayid
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkTablet.PlugAndPlayID
 - IInkTablet.get_PlugAndPlayID
 - IInkTablet.get_PlugAndPlayID
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkTablet::get_PlugAndPlayId


## -description


Gets a string representation of the Plug and Play identifier of the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object.
        

This property is read-only.


## -parameters


## -remarks



The property value is based upon the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538868">HIDD_ATTRIBUTES</a><b>ProductID</b> member. The manufacturer of the tablet device is responsible for adding this string. The property value is empty if the tablet device does not have an identifier.

<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: WM_ACTIVATE, WM_ACTIVATEAPP, WMNCACTIVATE, WM_PAINT; WM_SYSCOMMAND if <b>wParam</b> is set to SC_HOTKEY or SC_TASKLIST; and WM_SYSKEYDOWN (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets</a>
 

 


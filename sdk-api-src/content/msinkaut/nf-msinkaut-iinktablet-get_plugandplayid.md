---
UID: NF:msinkaut.IInkTablet.get_PlugAndPlayId
title: IInkTablet::get_PlugAndPlayId (msinkaut.h)
description: Gets a string representation of the Plug and Play identifier of the IInkTablet object.
helpviewer_keywords: ["5b33bd06-fee3-41b0-b3c1-d16b43685c60","IInkTablet interface [Tablet PC]","PlugAndPlayID property","IInkTablet.PlugAndPlayID","IInkTablet.get_PlugAndPlayID","IInkTablet.get_PlugAndPlayId","IInkTablet::PlugAndPlayID","IInkTablet::get_PlugAndPlayID","IInkTablet::get_PlugAndPlayId","PlugAndPlayID property [Tablet PC]","PlugAndPlayID property [Tablet PC]","IInkTablet interface","get_PlugAndPlayId","msinkaut/IInkTablet::PlugAndPlayID","msinkaut/IInkTablet::get_PlugAndPlayID","tablet.iinktablet_plugandplayid"]
old-location: tablet\iinktablet_plugandplayid.htm
tech.root: tablet
ms.assetid: 5b33bd06-fee3-41b0-b3c1-d16b43685c60
ms.date: 12/05/2018
ms.keywords: 5b33bd06-fee3-41b0-b3c1-d16b43685c60, IInkTablet interface [Tablet PC],PlugAndPlayID property, IInkTablet.PlugAndPlayID, IInkTablet.get_PlugAndPlayID, IInkTablet.get_PlugAndPlayId, IInkTablet::PlugAndPlayID, IInkTablet::get_PlugAndPlayID, IInkTablet::get_PlugAndPlayId, PlugAndPlayID property [Tablet PC], PlugAndPlayID property [Tablet PC],IInkTablet interface, get_PlugAndPlayId, msinkaut/IInkTablet::PlugAndPlayID, msinkaut/IInkTablet::get_PlugAndPlayID, tablet.iinktablet_plugandplayid
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
 - IInkTablet::get_PlugAndPlayId
 - msinkaut/IInkTablet::get_PlugAndPlayId
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
 - IInkTablet.PlugAndPlayID
 - IInkTablet.get_PlugAndPlayID
 - IInkTablet.get_PlugAndPlayID
---

# IInkTablet::get_PlugAndPlayId


## -description

Gets a string representation of the Plug and Play identifier of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object.
        

This property is read-only.

## -parameters

## -remarks

The property value is based upon the <a href="/windows-hardware/drivers/ddi/content/hidsdi/ns-hidsdi-_hidd_attributes">HIDD_ATTRIBUTES</a><b>ProductID</b> member. The manufacturer of the tablet device is responsible for adding this string. The property value is empty if the tablet device does not have an identifier.

<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: WM_ACTIVATE, WM_ACTIVATEAPP, WMNCACTIVATE, WM_PAINT; WM_SYSCOMMAND if <b>wParam</b> is set to SC_HOTKEY or SC_TASKLIST; and WM_SYSKEYDOWN (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications. </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms704832(v=vs.85)">InkTablets</a>
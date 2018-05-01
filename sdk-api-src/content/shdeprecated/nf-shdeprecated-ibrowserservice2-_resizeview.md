---
UID: NF:shdeprecated.IBrowserService2._ResizeView
title: IBrowserService2::_ResizeView method
author: windows-driver-content
description: Deprecated. Calls IBrowserService2::_UpdateViewRectSize, then updates the browser view by using IOleInPlaceActiveObject::ResizeBorder.
old-location: shell\IBrowserService2__ResizeView.htm
old-project: shell
ms.assetid: 12b38906-f22a-490d-9b2f-192eb43a8305
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IBrowserService2, IBrowserService2 interface [Windows Shell], _ResizeView method, IBrowserService2::_ResizeView, _ResizeView method [Windows Shell], _ResizeView method [Windows Shell], IBrowserService2 interface, _ResizeView,IBrowserService2._ResizeView, shdeprecated/IBrowserService2::_ResizeView, shell.IBrowserService2__ResizeView, zone_IBrowserService2__ResizeView
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	IBrowserService2._ResizeView
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_ResizeView method


## -description


Deprecated. Calls <a href="https://msdn.microsoft.com/92860c13-cb67-4499-90fe-2b0254ae25c7">IBrowserService2::_UpdateViewRectSize</a>, then updates the browser view by using <a href="https://msdn.microsoft.com/240d2ae5-abce-4bea-969e-f47780908bbb">IOleInPlaceActiveObject::ResizeBorder</a>.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




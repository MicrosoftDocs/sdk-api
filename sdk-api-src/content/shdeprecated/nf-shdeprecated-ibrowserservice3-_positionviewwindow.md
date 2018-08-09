---
UID: NF:shdeprecated.IBrowserService3._PositionViewWindow
title: IBrowserService3::_PositionViewWindow
author: windows-sdk-content
description: Deprecated. Used in view size negotiations. This method is called by _UpdateViewRectSize after determining the available dimensions.
old-location: shell\IBrowserService3__PositionViewWindow.htm
old-project: shell
ms.assetid: 310885e5-b08d-4699-9dee-244efa49dfd1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IBrowserService3 interface [Windows Shell],_PositionViewWindow method, IBrowserService3._PositionViewWindow, IBrowserService3::_PositionViewWindow, _PositionViewWindow, _PositionViewWindow method [Windows Shell], _PositionViewWindow method [Windows Shell],IBrowserService3 interface, shdeprecated/IBrowserService3::_PositionViewWindow, shell.IBrowserService3__PositionViewWindow, zone_IBrowserService3__PositionViewWindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BNSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService3._PositionViewWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.0
---

# IBrowserService3::_PositionViewWindow


## -description


Deprecated. Used in view size negotiations. This method is called by <a href="https://msdn.microsoft.com/92860c13-cb67-4499-90fe-2b0254ae25c7">_UpdateViewRectSize</a> after determining the available dimensions.


## -parameters




### -param hwnd

Type: <b>HWND</b>

The handle of the view window.


### -param prc

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the available dimensions.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




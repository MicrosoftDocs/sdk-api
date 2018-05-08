---
UID: NF:shdeprecated.IBrowserService2._GetEffectiveClientArea
title: IBrowserService2::_GetEffectiveClientArea
author: windows-driver-content
description: Deprecated. Used with IBrowserService2::_GetViewBorderRect to negotiate the dimensions of the browser view.
old-location: shell\IBrowserService2__GetEffectiveClientArea.htm
old-project: shell
ms.assetid: c0c53cd4-4b85-42d5-98c3-22ef46644a3f
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_GetEffectiveClientArea method, IBrowserService2._GetEffectiveClientArea, IBrowserService2::_GetEffectiveClientArea, _GetEffectiveClientArea, _GetEffectiveClientArea method [Windows Shell], _GetEffectiveClientArea method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_GetEffectiveClientArea, shell.IBrowserService2__GetEffectiveClientArea, zone_IBrowserService2__GetEffectiveClientArea
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
-	IBrowserService2._GetEffectiveClientArea
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_GetEffectiveClientArea


## -description


Deprecated. Used with <a href="https://msdn.microsoft.com/62ede825-a4f3-47bc-a9dd-9b651bde1ec5">IBrowserService2::_GetViewBorderRect</a> to negotiate the dimensions of the browser view.


## -parameters




### -param lprectBorder [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure indicating the dimensions of the available client area.


### -param hmon [in]

Type: <b>HMONITOR</b>

The handle of the monitor on which the view is displayed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c43c1401-52d3-485e-a418-205df5737040">HMONITOR and the Device Context</a>



<a href="https://msdn.microsoft.com/5c100b60-ef2e-4044-9f06-c1d01bcd88d2">IBrowserService2</a>
 

 


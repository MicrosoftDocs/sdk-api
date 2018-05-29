---
UID: NF:shdeprecated.IBrowserService2._GetViewBorderRect
title: IBrowserService2::_GetViewBorderRect
author: windows-sdk-content
description: Deprecated. Used with IBrowserService2::_GetEffectiveClientArea to negotiate the size and position of the browser view.
old-location: shell\IBrowserService2__GetViewBorderRect.htm
old-project: shell
ms.assetid: 62ede825-a4f3-47bc-a9dd-9b651bde1ec5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_GetViewBorderRect method, IBrowserService2._GetViewBorderRect, IBrowserService2::_GetViewBorderRect, _GetViewBorderRect, _GetViewBorderRect method [Windows Shell], _GetViewBorderRect method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_GetViewBorderRect, shell.IBrowserService2__GetViewBorderRect, zone_IBrowserService2__GetViewBorderRect
ms.prod: windows
ms.technology: windows-sdk
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
-	IBrowserService2._GetViewBorderRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_GetViewBorderRect


## -description


Deprecated. Used with <a href="https://msdn.microsoft.com/c0c53cd4-4b85-42d5-98c3-22ef46644a3f">IBrowserService2::_GetEffectiveClientArea</a> to negotiate the size and position of the browser view.


## -parameters




### -param prc [in, out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure stating the dimensions of the browser view's border.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by <a href="https://msdn.microsoft.com/738aa84d-9586-493e-8a50-e8e1918198e6">IBrowserService2::GetViewRect</a>.




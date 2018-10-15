---
UID: NF:shdeprecated.IBrowserService2._ResizeNextBorder
title: IBrowserService2::_ResizeNextBorder
author: windows-sdk-content
description: Deprecated. Resizes the border of the browser view in response to the addition or removal of toolbars.
old-location: shell\IBrowserService2__ResizeNextBorder.htm
tech.root: shell
ms.assetid: 9d7c618a-2948-44cf-8e47-96d33c08c9a5
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_ResizeNextBorder method, IBrowserService2._ResizeNextBorder, IBrowserService2::_ResizeNextBorder, _ResizeNextBorder, _ResizeNextBorder method [Windows Shell], _ResizeNextBorder method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_ResizeNextBorder, shell.IBrowserService2__ResizeNextBorder, zone_IBrowserService2__ResizeNextBorder
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2._ResizeNextBorder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_ResizeNextBorder


## -description


Deprecated. Resizes the border of the browser view in response to the addition or removal of toolbars.


## -parameters




### -param itb [in]

Type: <b>UINT</b>

The index of the toolbar that was added or removed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The implementation of this method calls <a href="https://msdn.microsoft.com/850025c0-96a0-4b7b-aa87-18325b0aecab">IBrowserService2::_ResizeNextBorderHelper</a>.




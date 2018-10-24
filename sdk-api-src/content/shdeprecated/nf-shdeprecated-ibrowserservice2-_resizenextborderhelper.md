---
UID: NF:shdeprecated.IBrowserService2._ResizeNextBorderHelper
title: IBrowserService2::_ResizeNextBorderHelper
author: windows-sdk-content
description: Deprecated. A helper method used by the implementation of IBrowserService2::_ResizeNextBorder.
old-location: shell\IBrowserService2__ResizeNextBorderHelper.htm
tech.root: shell
ms.assetid: 850025c0-96a0-4b7b-aa87-18325b0aecab
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_ResizeNextBorderHelper method, IBrowserService2._ResizeNextBorderHelper, IBrowserService2::_ResizeNextBorderHelper, _ResizeNextBorderHelper, _ResizeNextBorderHelper method [Windows Shell], _ResizeNextBorderHelper method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_ResizeNextBorderHelper, shell.IBrowserService2__ResizeNextBorderHelper, zone_IBrowserService2__ResizeNextBorderHelper
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
 - IBrowserService2._ResizeNextBorderHelper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_ResizeNextBorderHelper


## -description


Deprecated. A helper method used by the implementation of <a href="https://msdn.microsoft.com/9d7c618a-2948-44cf-8e47-96d33c08c9a5">IBrowserService2::_ResizeNextBorder</a>.


## -parameters




### -param itb [in]

Type: <b>UINT</b>

The index of the browser toolbar.


### -param bUseHmonitor [in]

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates whether to use an <b>HMONITOR</b> to determine the display. <b>TRUE</b> to use the <b>HMONITOR</b>; <b>FALSE</b> to ignore the particular display in the size determination.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




---
UID: NF:shdeprecated.IBrowserService2.GetViewRect
title: IBrowserService2::GetViewRect
author: windows-sdk-content
description: Deprecated. Retrieves a value that is used to negotiate the allowed size of the window.
old-location: shell\IBrowserService2_GetViewRect.htm
tech.root: shell
ms.assetid: 738aa84d-9586-493e-8a50-e8e1918198e6
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetViewRect, GetViewRect method [Windows Shell], GetViewRect method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],GetViewRect method, IBrowserService2.GetViewRect, IBrowserService2::GetViewRect, shdeprecated/IBrowserService2::GetViewRect, shell.IBrowserService2_GetViewRect, zone_IBrowserService2_GetViewRect
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
 - IBrowserService2.GetViewRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::GetViewRect


## -description


Deprecated. Retrieves a value that is used to negotiate the allowed size of the window.


## -parameters




### -param prc [in, out]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a <b>RECT</b> structure that receives the allowed dimensions.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




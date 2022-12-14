---
UID: NF:shdeprecated.IBrowserService2.GetViewRect
title: IBrowserService2::GetViewRect (shdeprecated.h)
description: Deprecated. Retrieves a value that is used to negotiate the allowed size of the window.
helpviewer_keywords: ["GetViewRect","GetViewRect method [Windows Shell]","GetViewRect method [Windows Shell]","IBrowserService2 interface","IBrowserService2 interface [Windows Shell]","GetViewRect method","IBrowserService2.GetViewRect","IBrowserService2::GetViewRect","shdeprecated/IBrowserService2::GetViewRect","shell.IBrowserService2_GetViewRect","zone_IBrowserService2_GetViewRect"]
old-location: shell\IBrowserService2_GetViewRect.htm
tech.root: shell
ms.assetid: 738aa84d-9586-493e-8a50-e8e1918198e6
ms.date: 12/05/2018
ms.keywords: GetViewRect, GetViewRect method [Windows Shell], GetViewRect method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],GetViewRect method, IBrowserService2.GetViewRect, IBrowserService2::GetViewRect, shdeprecated/IBrowserService2::GetViewRect, shell.IBrowserService2_GetViewRect, zone_IBrowserService2_GetViewRect
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService2::GetViewRect
 - shdeprecated/IBrowserService2::GetViewRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2.GetViewRect
---

# IBrowserService2::GetViewRect


## -description

Deprecated. Retrieves a value that is used to negotiate the allowed size of the window.

## -parameters

### -param prc [in, out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <b>RECT</b> structure that receives the allowed dimensions.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


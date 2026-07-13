---
UID: NF:ddraw.IDirectDrawColorControl.GetColorControls
title: IDirectDrawColorControl::GetColorControls (ddraw.h)
description: Retrieves the current color-control settings that are associated with an overlay or a primary surface.
helpviewer_keywords: ["GetColorControls","GetColorControls method [DirectDraw]","GetColorControls method [DirectDraw]","IDirectDrawColorControl interface","IDirectDrawColorControl interface [DirectDraw]","GetColorControls method","IDirectDrawColorControl.GetColorControls","IDirectDrawColorControl::GetColorControls","ddraw/IDirectDrawColorControl::GetColorControls","directdraw.idirectdrawcolorcontrol_getcolorcontrols"]
old-location: directdraw\idirectdrawcolorcontrol_getcolorcontrols.htm
tech.root: directdraw
ms.assetid: 16ac7bef-e88c-47da-8db9-9e6258a381a0
ms.date: 12/05/2018
ms.keywords: GetColorControls, GetColorControls method [DirectDraw], GetColorControls method [DirectDraw],IDirectDrawColorControl interface, IDirectDrawColorControl interface [DirectDraw],GetColorControls method, IDirectDrawColorControl.GetColorControls, IDirectDrawColorControl::GetColorControls, ddraw/IDirectDrawColorControl::GetColorControls, directdraw.idirectdrawcolorcontrol_getcolorcontrols
f1_keywords:
- ddraw/IDirectDrawColorControl.GetColorControls
dev_langs:
- c++
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ddraw.dll
api_name:
- IDirectDrawColorControl.GetColorControls
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the current color-control settings that are associated with an overlay or a primary surface.

## -parameters

### -param unnamedParam1 [in, out]

A pointer to a <a href="/previous-versions/windows/hardware/drivers/ff549237(v=vs.85)">DDCOLORCONTROL</a> structure that receives the current control settings.

## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



The <b>dwFlags</b> member of the <a href="/previous-versions/windows/hardware/drivers/ff549237(v=vs.85)">DDCOLORCONTROL</a> structure indicates which of the color-control options are supported.







## -see-also




<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawcolorcontrol">IDirectDrawColorControl</a>
 

 
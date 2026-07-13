---
UID: NF:shobjidl_core.IPreviewHandlerVisuals.SetFont
title: IPreviewHandlerVisuals::SetFont (shobjidl_core.h)
description: Sets the font attributes to be used for text within the preview handler.
helpviewer_keywords: ["IPreviewHandlerVisuals interface [Windows Shell]","SetFont method","IPreviewHandlerVisuals.SetFont","IPreviewHandlerVisuals::SetFont","SetFont","SetFont method [Windows Shell]","SetFont method [Windows Shell]","IPreviewHandlerVisuals interface","_shell_IPreviewHandlerVisuals_SetFont","shell.IPreviewHandlerVisuals_SetFont","shobjidl_core/IPreviewHandlerVisuals::SetFont"]
old-location: shell\IPreviewHandlerVisuals_SetFont.htm
tech.root: shell
ms.assetid: f329e2ad-ec79-4542-b7ef-ff38bda6e8cc
ms.date: 12/05/2018
ms.keywords: IPreviewHandlerVisuals interface [Windows Shell],SetFont method, IPreviewHandlerVisuals.SetFont, IPreviewHandlerVisuals::SetFont, SetFont, SetFont method [Windows Shell], SetFont method [Windows Shell],IPreviewHandlerVisuals interface, _shell_IPreviewHandlerVisuals_SetFont, shell.IPreviewHandlerVisuals_SetFont, shobjidl_core/IPreviewHandlerVisuals::SetFont
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
ms.custom: 19H1
f1_keywords:
 - IPreviewHandlerVisuals::SetFont
 - shobjidl_core/IPreviewHandlerVisuals::SetFont
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IPreviewHandlerVisuals.SetFont
---

# IPreviewHandlerVisuals::SetFont


## -description

Sets the font attributes to be used for text within the preview handler.

## -parameters

### -param plf [in]

Type: <b>const LOGFONTW*</b>

A pointer to a <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa741231(v=vs.85)">LOGFONTW Structure</a> containing the necessary attributes for the font to use.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  These are suggestions. It is not compulsory for this method to be called. The preview handlers must be able to make their own decisions.</div>
<div> </div>
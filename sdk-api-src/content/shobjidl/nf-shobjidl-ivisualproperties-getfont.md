---
UID: NF:shobjidl.IVisualProperties.GetFont
title: IVisualProperties::GetFont (shobjidl.h)
description: Gets the current attributes set on the font.
helpviewer_keywords: ["GetFont","GetFont method [Windows Shell]","GetFont method [Windows Shell]","IVisualProperties interface","IVisualProperties interface [Windows Shell]","GetFont method","IVisualProperties.GetFont","IVisualProperties::GetFont","_shell_IVisualProperties_GetFont","shell.IVisualProperties_GetFont","shobjidl/IVisualProperties::GetFont"]
old-location: shell\IVisualProperties_GetFont.htm
tech.root: shell
ms.assetid: d12e2091-37cb-4a9e-abfc-8795d18bddd2
ms.date: 12/05/2018
ms.keywords: GetFont, GetFont method [Windows Shell], GetFont method [Windows Shell],IVisualProperties interface, IVisualProperties interface [Windows Shell],GetFont method, IVisualProperties.GetFont, IVisualProperties::GetFont, _shell_IVisualProperties_GetFont, shell.IVisualProperties_GetFont, shobjidl/IVisualProperties::GetFont
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVisualProperties::GetFont
 - shobjidl/IVisualProperties::GetFont
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IVisualProperties.GetFont
---

# IVisualProperties::GetFont


## -description

Gets the current attributes set on the font.

## -parameters

### -param plf [out]

Type: <b>LOGFONTW*</b>

A pointer to a <a href="/windows/win32/api/dimm/ns-dimm-logfonta">LOGFONT</a> structure that, when this method returns successfully, receives the current attributes of the font.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


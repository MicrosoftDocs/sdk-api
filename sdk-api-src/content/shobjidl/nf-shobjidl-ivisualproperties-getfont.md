---
UID: NF:shobjidl.IVisualProperties.GetFont
title: IVisualProperties::GetFont
author: windows-sdk-content
description: Gets the current attributes set on the font.
old-location: shell\IVisualProperties_GetFont.htm
old-project: shell
ms.assetid: d12e2091-37cb-4a9e-abfc-8795d18bddd2
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetFont, GetFont method [Windows Shell], GetFont method [Windows Shell],IVisualProperties interface, IVisualProperties interface [Windows Shell],GetFont method, IVisualProperties.GetFont, IVisualProperties::GetFont, _shell_IVisualProperties_GetFont, shell.IVisualProperties_GetFont, shobjidl/IVisualProperties::GetFont
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IVisualProperties.GetFont
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IVisualProperties::GetFont


## -description


Gets the current attributes set on the font.


## -parameters




### -param plf [out]

Type: <b>LOGFONTW*</b>

A pointer to a <a href="https://msdn.microsoft.com/759c54d9-5b8f-4b48-8380-79e7bcae5bdb">LOGFONT</a> structure that, when this method returns successfully, receives the current attributes of the font.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




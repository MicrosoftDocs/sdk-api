---
UID: NF:shobjidl.IVisualProperties.SetColor
title: IVisualProperties::SetColor
author: windows-sdk-content
description: Sets the color, as specified.
old-location: shell\IVisualProperties_SetColor.htm
old-project: shell
ms.assetid: 24e351af-687d-454a-9f0a-e7c07175dbd3
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IVisualProperties interface [Windows Shell],SetColor method, IVisualProperties.SetColor, IVisualProperties::SetColor, SetColor, SetColor method [Windows Shell], SetColor method [Windows Shell],IVisualProperties interface, _shell_IVisualProperties_SetColor, shell.IVisualProperties_SetColor, shobjidl/IVisualProperties::SetColor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IVisualProperties.SetColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IVisualProperties::SetColor


## -description


Sets the color, as specified.


## -parameters




### -param vpcf [in]

Type: <b><a href="https://msdn.microsoft.com/438fb7ee-c0ce-4c20-9dbb-51593005d3ad">VPCOLORFLAGS</a></b>

The color flags. See <a href="https://msdn.microsoft.com/438fb7ee-c0ce-4c20-9dbb-51593005d3ad">VPCOLORFLAGS</a>.


### -param cr [in]

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

A value of type <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




---
UID: NF:shobjidl.IVisualProperties.GetColor
title: IVisualProperties::GetColor
author: windows-sdk-content
description: Gets the color, as specified.
old-location: shell\IVisualProperties_GetColor.htm
tech.root: shell
ms.assetid: 538ac798-7722-434f-88bd-a7655d4c470c
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: GetColor, GetColor method [Windows Shell], GetColor method [Windows Shell],IVisualProperties interface, IVisualProperties interface [Windows Shell],GetColor method, IVisualProperties.GetColor, IVisualProperties::GetColor, _shell_IVisualProperties_GetColor, shell.IVisualProperties_GetColor, shobjidl/IVisualProperties::GetColor
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IVisualProperties.GetColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVisualProperties::GetColor


## -description


Gets the color, as specified.


## -parameters




### -param vpcf [in]

Type: <b><a href="https://msdn.microsoft.com/438fb7ee-c0ce-4c20-9dbb-51593005d3ad">VPCOLORFLAGS</a></b>

The color flags. See <a href="https://msdn.microsoft.com/438fb7ee-c0ce-4c20-9dbb-51593005d3ad">VPCOLORFLAGS</a>



### -param pcr [out]

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>*</b>

A pointer to a value of type <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




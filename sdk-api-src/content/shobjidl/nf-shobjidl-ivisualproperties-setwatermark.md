---
UID: NF:shobjidl.IVisualProperties.SetWatermark
title: IVisualProperties::SetWatermark
author: windows-sdk-content
description: Provides a bitmap to use as a watermark.
old-location: shell\IVisualProperties_SetWatermark.htm
old-project: shell
ms.assetid: 14ce62f7-b464-4e52-8441-35f613b6c844
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IVisualProperties interface [Windows Shell],SetWatermark method, IVisualProperties.SetWatermark, IVisualProperties::SetWatermark, SetWatermark, SetWatermark method [Windows Shell], SetWatermark method [Windows Shell],IVisualProperties interface, _shell_IVisualProperties_SetWatermark, shell.IVisualProperties_SetWatermark, shobjidl/IVisualProperties::SetWatermark
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
 - IVisualProperties.SetWatermark
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IVisualProperties::SetWatermark


## -description


Provides a bitmap to use as a watermark.


## -parameters




### -param hbmp [in]

Type: <b>HBITMAP</b>

A handle to the bitmap.


### -param vpwf [in]

Type: <b><a href="https://msdn.microsoft.com/e54db88e-c334-442b-8ab5-6004176aab41">VPWATERMARKFLAGS</a></b>


<a href="https://msdn.microsoft.com/e54db88e-c334-442b-8ab5-6004176aab41">VPWATERMARKFLAGS</a> flags that customize the watermark.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




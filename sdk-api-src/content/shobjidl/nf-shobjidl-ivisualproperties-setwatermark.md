---
UID: NF:shobjidl.IVisualProperties.SetWatermark
title: IVisualProperties::SetWatermark (shobjidl.h)

description: Provides a bitmap to use as a watermark.
old-location: shell\IVisualProperties_SetWatermark.htm
tech.root: shell
ms.assetid: 14ce62f7-b464-4e52-8441-35f613b6c844

ms.date: 12/05/2018
ms.keywords: IVisualProperties interface [Windows Shell],SetWatermark method, IVisualProperties.SetWatermark, IVisualProperties::SetWatermark, SetWatermark, SetWatermark method [Windows Shell], SetWatermark method [Windows Shell],IVisualProperties interface, _shell_IVisualProperties_SetWatermark, shell.IVisualProperties_SetWatermark, shobjidl/IVisualProperties::SetWatermark
ms.topic: method
f1_keywords: 
 - "shobjidl/IVisualProperties.SetWatermark"
dev_langs:
 - c++
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
 - IVisualProperties.SetWatermark
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVisualProperties::SetWatermark


## -description


Provides a bitmap to use as a watermark.


## -parameters




### -param hbmp [in]

Type: <b>HBITMAP</b>

A handle to the bitmap.


### -param vpwf [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/ne-shobjidl-vpwatermarkflags">VPWATERMARKFLAGS</a></b>


<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/ne-shobjidl-vpwatermarkflags">VPWATERMARKFLAGS</a> flags that customize the watermark.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




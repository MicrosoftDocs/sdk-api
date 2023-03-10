---
UID: NF:micaut.IMathInputControl.GetPreviewHeight
title: IMathInputControl::GetPreviewHeight (micaut.h)
description: Retrieves the height in pixels of the preview area.
helpviewer_keywords: ["GetPreviewHeight","GetPreviewHeight method [Tablet PC]","GetPreviewHeight method [Tablet PC]","IMathInputControl interface","IMathInputControl interface [Tablet PC]","GetPreviewHeight method","IMathInputControl.GetPreviewHeight","IMathInputControl::GetPreviewHeight","micaut/IMathInputControl::GetPreviewHeight","tablet.imathinputcontrol_getpreviewheight"]
old-location: tablet\imathinputcontrol_getpreviewheight.htm
tech.root: tablet
ms.assetid: 3b3404f5-b775-483f-b3a9-9467c937226b
ms.date: 12/05/2018
ms.keywords: GetPreviewHeight, GetPreviewHeight method [Tablet PC], GetPreviewHeight method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],GetPreviewHeight method, IMathInputControl.GetPreviewHeight, IMathInputControl::GetPreviewHeight, micaut/IMathInputControl::GetPreviewHeight, tablet.imathinputcontrol_getpreviewheight
req.header: micaut.h
req.include-header: Micaut.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Micaut.idl
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
 - IMathInputControl::GetPreviewHeight
 - micaut/IMathInputControl::GetPreviewHeight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl.GetPreviewHeight
---

# IMathInputControl::GetPreviewHeight


## -description

Retrieves the height in pixels of the preview area.

## -parameters

### -param Height [out]

The height in pixels of the preview area.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Manually resizing the control can affect the height of the result-preview area.

## -see-also

<a href="/windows/desktop/tablet/customizing-the-math-input-control">Customizing the Math Input Control</a>



<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>



<a href="/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-setpreviewheight">SetPreviewHeight</a>
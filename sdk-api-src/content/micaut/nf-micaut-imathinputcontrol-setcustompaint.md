---
UID: NF:micaut.IMathInputControl.SetCustomPaint
title: IMathInputControl::SetCustomPaint (micaut.h)
description: Determines whether a button or background has custom painting.
helpviewer_keywords: ["IMathInputControl interface [Tablet PC]","SetCustomPaint method","IMathInputControl.SetCustomPaint","IMathInputControl::SetCustomPaint","SetCustomPaint","SetCustomPaint method [Tablet PC]","SetCustomPaint method [Tablet PC]","IMathInputControl interface","micaut/IMathInputControl::SetCustomPaint","tablet.imathinputcontrol_setcustompaint"]
old-location: tablet\imathinputcontrol_setcustompaint.htm
tech.root: tablet
ms.assetid: f734b73c-88a9-45d0-a657-ff048d1f5ffe
ms.date: 12/05/2018
ms.keywords: IMathInputControl interface [Tablet PC],SetCustomPaint method, IMathInputControl.SetCustomPaint, IMathInputControl::SetCustomPaint, SetCustomPaint, SetCustomPaint method [Tablet PC], SetCustomPaint method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::SetCustomPaint, tablet.imathinputcontrol_setcustompaint
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
 - IMathInputControl::SetCustomPaint
 - micaut/IMathInputControl::SetCustomPaint
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
 - IMathInputControl.SetCustomPaint
---

# IMathInputControl::SetCustomPaint


## -description

Determines whether a button or background has custom painting.

## -parameters

### -param Element [in]

The identifier for a button or background.

### -param Paint [in]

<b>VARIANT_TRUE</b> to enable custom painting for the specified UI element; otherwise, <b>VARIANT_FALSE</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If custom painting is enabled, the button or background will be rendered at least partially—and possibly completely—by the container.

## -see-also

<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>
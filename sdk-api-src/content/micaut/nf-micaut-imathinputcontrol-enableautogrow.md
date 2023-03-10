---
UID: NF:micaut.IMathInputControl.EnableAutoGrow
title: IMathInputControl::EnableAutoGrow (micaut.h)
description: Determines whether the control automatically grows when input is entered beyond the control's current range.
helpviewer_keywords: ["EnableAutoGrow","EnableAutoGrow method [Tablet PC]","EnableAutoGrow method [Tablet PC]","IMathInputControl interface","IMathInputControl interface [Tablet PC]","EnableAutoGrow method","IMathInputControl.EnableAutoGrow","IMathInputControl::EnableAutoGrow","micaut/IMathInputControl::EnableAutoGrow","tablet.imathinputcontrol_enableautogrow"]
old-location: tablet\imathinputcontrol_enableautogrow.htm
tech.root: tablet
ms.assetid: 23eae5ee-8f3d-4f54-9c30-b29f0c14ba7f
ms.date: 12/05/2018
ms.keywords: EnableAutoGrow, EnableAutoGrow method [Tablet PC], EnableAutoGrow method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],EnableAutoGrow method, IMathInputControl.EnableAutoGrow, IMathInputControl::EnableAutoGrow, micaut/IMathInputControl::EnableAutoGrow, tablet.imathinputcontrol_enableautogrow
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
 - IMathInputControl::EnableAutoGrow
 - micaut/IMathInputControl::EnableAutoGrow
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
 - IMathInputControl.EnableAutoGrow
---

# IMathInputControl::EnableAutoGrow


## -description

Determines whether the control automatically grows when input is entered beyond the control's current range.

## -parameters

### -param AutoGrow [in]

<b>VARIANT_TRUE</b> to enable automatic growth; otherwise, <b>VARIANT_FALSE</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Automatic growth is enabled by default.

## -see-also

<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>
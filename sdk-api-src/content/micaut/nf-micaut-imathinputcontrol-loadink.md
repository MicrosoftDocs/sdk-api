---
UID: NF:micaut.IMathInputControl.LoadInk
title: IMathInputControl::LoadInk (micaut.h)
description: Processes ink and triggers recognition.
helpviewer_keywords: ["IMathInputControl interface [Tablet PC]","LoadInk method","IMathInputControl.LoadInk","IMathInputControl::LoadInk","LoadInk","LoadInk method [Tablet PC]","LoadInk method [Tablet PC]","IMathInputControl interface","micaut/IMathInputControl::LoadInk","tablet.imathinputcontrol_loadink"]
old-location: tablet\imathinputcontrol_loadink.htm
tech.root: tablet
ms.assetid: 3313cb16-3400-48d5-8ba0-b3bd593b37ea
ms.date: 12/05/2018
ms.keywords: IMathInputControl interface [Tablet PC],LoadInk method, IMathInputControl.LoadInk, IMathInputControl::LoadInk, LoadInk, LoadInk method [Tablet PC], LoadInk method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::LoadInk, tablet.imathinputcontrol_loadink
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
 - IMathInputControl::LoadInk
 - micaut/IMathInputControl::LoadInk
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
 - IMathInputControl.LoadInk
---

# IMathInputControl::LoadInk


## -description

Processes ink and triggers recognition.

## -parameters

### -param Ink [in]

The ink object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method will only work when the control is visible.
When that ink exceeds the control's current size, and automatic growth is enabled, the control tries to accommodate the input. If the control cannot supply enough space, ink is proportionally shrunk to fit the maximum available size.

## -see-also

<a href="/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-enableautogrow">EnableAutoGrow</a>



<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>
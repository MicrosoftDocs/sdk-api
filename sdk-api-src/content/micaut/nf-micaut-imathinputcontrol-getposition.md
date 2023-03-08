---
UID: NF:micaut.IMathInputControl.GetPosition
title: IMathInputControl::GetPosition (micaut.h)
description: Retrieves the position and size of the control.
helpviewer_keywords: ["GetPosition","GetPosition method [Tablet PC]","GetPosition method [Tablet PC]","IMathInputControl interface","IMathInputControl interface [Tablet PC]","GetPosition method","IMathInputControl.GetPosition","IMathInputControl::GetPosition","micaut/IMathInputControl::GetPosition","tablet.imathinputcontrol_getposition"]
old-location: tablet\imathinputcontrol_getposition.htm
tech.root: tablet
ms.assetid: 4928f92d-7150-434c-abe4-d65a48ce1a56
ms.date: 12/05/2018
ms.keywords: GetPosition, GetPosition method [Tablet PC], GetPosition method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],GetPosition method, IMathInputControl.GetPosition, IMathInputControl::GetPosition, micaut/IMathInputControl::GetPosition, tablet.imathinputcontrol_getposition
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
 - IMathInputControl::GetPosition
 - micaut/IMathInputControl::GetPosition
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
 - IMathInputControl.GetPosition
---

# IMathInputControl::GetPosition


## -description

Retrieves the position and size of the control.

## -parameters

### -param Left [out]

The leftmost position of the control.

### -param Top [out]

The highest position of the control.

### -param Right [out]

The rightmost position of the control.

### -param Bottom [out]

The lowest position of the control.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method returns the control size and position even if the control is not visible.

This method returns the minimal possible width and height of the control if it is called immediately after creation of the control.

## -see-also

<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>



<a href="/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-setposition">SetPosition</a>
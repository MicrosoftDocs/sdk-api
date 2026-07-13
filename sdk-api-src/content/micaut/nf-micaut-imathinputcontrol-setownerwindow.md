---
UID: NF:micaut.IMathInputControl.SetOwnerWindow
title: IMathInputControl::SetOwnerWindow (micaut.h)
description: Modifies the window that owns this control.
helpviewer_keywords: ["IMathInputControl interface [Tablet PC]","SetOwnerWindow method","IMathInputControl.SetOwnerWindow","IMathInputControl::SetOwnerWindow","SetOwnerWindow","SetOwnerWindow method [Tablet PC]","SetOwnerWindow method [Tablet PC]","IMathInputControl interface","micaut/IMathInputControl::SetOwnerWindow","tablet.imathinputcontrol_setownerwindow"]
old-location: tablet\imathinputcontrol_setownerwindow.htm
tech.root: tablet
ms.assetid: 2f92f731-3297-4da3-a2b9-18e1583c8b1d
ms.date: 12/05/2018
ms.keywords: IMathInputControl interface [Tablet PC],SetOwnerWindow method, IMathInputControl.SetOwnerWindow, IMathInputControl::SetOwnerWindow, SetOwnerWindow, SetOwnerWindow method [Tablet PC], SetOwnerWindow method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::SetOwnerWindow, tablet.imathinputcontrol_setownerwindow
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
 - IMathInputControl::SetOwnerWindow
 - micaut/IMathInputControl::SetOwnerWindow
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
 - IMathInputControl.SetOwnerWindow
---

# IMathInputControl::SetOwnerWindow


## -description

Modifies the window that owns this control.

## -parameters

### -param OwnerWindow [in]

A handle to the owner window.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The math input control always appears on top of the window that owns it.

## -see-also

<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>
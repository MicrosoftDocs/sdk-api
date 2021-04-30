---
UID: NF:shdeprecated.IExpDispSupport.OnTranslateAccelerator
title: IExpDispSupport::OnTranslateAccelerator (shdeprecated.h)
description: Deprecated. Instructs the control site to process the keystroke described in pMsg and modified by the flags in grfModifiers.
helpviewer_keywords: ["IExpDispSupport interface [Windows Shell]","OnTranslateAccelerator method","IExpDispSupport.OnTranslateAccelerator","IExpDispSupport::OnTranslateAccelerator","OnTranslateAccelerator","OnTranslateAccelerator method [Windows Shell]","OnTranslateAccelerator method [Windows Shell]","IExpDispSupport interface","shdeprecated/IExpDispSupport::OnTranslateAccelerator","shell.IExpDispSupport_OnTranslateAccelerator","zone_IExpDispSupport_OnTranslateAccelerator"]
old-location: shell\IExpDispSupport_OnTranslateAccelerator.htm
tech.root: shell
ms.assetid: 55f3b4dd-134d-49fe-a7f7-c6315971e902
ms.date: 12/05/2018
ms.keywords: IExpDispSupport interface [Windows Shell],OnTranslateAccelerator method, IExpDispSupport.OnTranslateAccelerator, IExpDispSupport::OnTranslateAccelerator, OnTranslateAccelerator, OnTranslateAccelerator method [Windows Shell], OnTranslateAccelerator method [Windows Shell],IExpDispSupport interface, shdeprecated/IExpDispSupport::OnTranslateAccelerator, shell.IExpDispSupport_OnTranslateAccelerator, zone_IExpDispSupport_OnTranslateAccelerator
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IExpDispSupport::OnTranslateAccelerator
 - shdeprecated/IExpDispSupport::OnTranslateAccelerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IExpDispSupport.OnTranslateAccelerator
---

# IExpDispSupport::OnTranslateAccelerator


## -description

Deprecated. Instructs the control site to process the keystroke described in <i>pMsg</i> and modified by the flags in <i>grfModifiers</i>.

## -parameters

### -param pMsg

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>*</b>

A pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that describes the keystroke to be processed.

### -param grfModifiers

Type: <b>DWORD</b>

Flags describing the state of the CTRL, ALT, and SHIFT keys. The value of the flags can be any valid <a href="/previous-versions/windows/desktop/legacy/ms683763(v=vs.85)">KEYMODIFIERS</a> enumeration value or values.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the container processed the message, <b>S_FALSE</b> if the container did not process the message, or <b>E_NOTIMPL</b> if the container does not implement accelerator support.
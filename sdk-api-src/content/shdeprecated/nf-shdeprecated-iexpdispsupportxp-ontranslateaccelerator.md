---
UID: NF:shdeprecated.IExpDispSupportXP.OnTranslateAccelerator
title: IExpDispSupportXP::OnTranslateAccelerator (shdeprecated.h)
description: Not implemented. (IExpDispSupportXP.OnTranslateAccelerator)
helpviewer_keywords: ["IExpDispSupportXP interface [Windows Shell]","OnTranslateAccelerator method","IExpDispSupportXP.OnTranslateAccelerator","IExpDispSupportXP::OnTranslateAccelerator","OnTranslateAccelerator","OnTranslateAccelerator method [Windows Shell]","OnTranslateAccelerator method [Windows Shell]","IExpDispSupportXP interface","_shell_IExpDispSupportXP_OnTranslateAccelerator","shdeprecated/IExpDispSupportXP::OnTranslateAccelerator","shell.IExpDispSupportXP_OnTranslateAccelerator"]
old-location: shell\IExpDispSupportXP_OnTranslateAccelerator.htm
tech.root: shell
ms.assetid: 7afdcd4d-76c6-41ff-b754-83068d5ca5cd
ms.date: 12/05/2018
ms.keywords: IExpDispSupportXP interface [Windows Shell],OnTranslateAccelerator method, IExpDispSupportXP.OnTranslateAccelerator, IExpDispSupportXP::OnTranslateAccelerator, OnTranslateAccelerator, OnTranslateAccelerator method [Windows Shell], OnTranslateAccelerator method [Windows Shell],IExpDispSupportXP interface, _shell_IExpDispSupportXP_OnTranslateAccelerator, shdeprecated/IExpDispSupportXP::OnTranslateAccelerator, shell.IExpDispSupportXP_OnTranslateAccelerator
req.header: shdeprecated.h
req.include-header: Shdeprecated.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
ms.custom: 19H1
f1_keywords:
 - IExpDispSupportXP::OnTranslateAccelerator
 - shdeprecated/IExpDispSupportXP::OnTranslateAccelerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shdeprecated.h
api_name:
 - IExpDispSupportXP.OnTranslateAccelerator
---

# IExpDispSupportXP::OnTranslateAccelerator


## -description

Not implemented.

## -parameters

### -param pMsg [in]

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>*</b>

Specifies a pointer to the MSG structure describing the keystroke to be processed.

### -param grfModifiers

Type: <b>DWORD</b>

Specifies the flags describing the state of the Control, Alt, and Shift keys. The value of the flag can be any valid <a href="/previous-versions/windows/desktop/legacy/ms683763(v=vs.85)">KEYMODIFIERS</a> enumeration values.

## -returns

Type: <b>HRESULT</b>

Returns <b>E_NOTIMPL</b>.

---
UID: NF:shobjidl_core.IInputObject2.TranslateAcceleratorGlobal
title: IInputObject2::TranslateAcceleratorGlobal (shobjidl_core.h)
author: windows-sdk-content
description: Handles global accelerators so that input objects can respond to the keyboard even when they are not active in the UI.
old-location: shell\IInputObject2_TranslateAcceleratorGlobal.htm
tech.root: shell
ms.assetid: f55f2671-7164-421e-9269-aa70e85180de
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInputObject2 interface [Windows Shell],TranslateAcceleratorGlobal method, IInputObject2.TranslateAcceleratorGlobal, IInputObject2::TranslateAcceleratorGlobal, TranslateAcceleratorGlobal, TranslateAcceleratorGlobal method [Windows Shell], TranslateAcceleratorGlobal method [Windows Shell],IInputObject2 interface, _shell_IInputObject2_TranslateAcceleratorGlobal, shell.IInputObject2_TranslateAcceleratorGlobal, shobjidl_core/IInputObject2::TranslateAcceleratorGlobal
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IInputObject2.TranslateAcceleratorGlobal"
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - shobjidl_core.h
api_name:
 - IInputObject2.TranslateAcceleratorGlobal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInputObject2::TranslateAcceleratorGlobal


## -description


Handles global accelerators so that input objects can respond to the keyboard even when they are not active in the UI.


## -parameters




### -param pMsg [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure that contains a keyboard message.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




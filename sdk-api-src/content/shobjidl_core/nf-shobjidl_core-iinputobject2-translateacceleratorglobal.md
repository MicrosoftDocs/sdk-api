---
UID: NF:shobjidl_core.IInputObject2.TranslateAcceleratorGlobal
title: IInputObject2::TranslateAcceleratorGlobal
author: windows-sdk-content
description: Handles global accelerators so that input objects can respond to the keyboard even when they are not active in the UI.
old-location: shell\IInputObject2_TranslateAcceleratorGlobal.htm
old-project: shell
ms.assetid: f55f2671-7164-421e-9269-aa70e85180de
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IInputObject2 interface [Windows Shell],TranslateAcceleratorGlobal method, IInputObject2.TranslateAcceleratorGlobal, IInputObject2::TranslateAcceleratorGlobal, TranslateAcceleratorGlobal, TranslateAcceleratorGlobal method [Windows Shell], TranslateAcceleratorGlobal method [Windows Shell],IInputObject2 interface, _shell_IInputObject2_TranslateAcceleratorGlobal, shell.IInputObject2_TranslateAcceleratorGlobal, shobjidl_core/IInputObject2::TranslateAcceleratorGlobal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IInputObject2.TranslateAcceleratorGlobal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IInputObject2::TranslateAcceleratorGlobal


## -description


Handles global accelerators so that input objects can respond to the keyboard even when they are not active in the UI.


## -parameters




### -param pMsg [in]

Type: <b><a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure that contains a keyboard message.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




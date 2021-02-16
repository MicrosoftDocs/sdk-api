---
UID: NF:tom.ITextDocument2.GetWindow
title: ITextDocument2::GetWindow (tom.h)
description: Gets the handle of the window that the Text Object Model (TOM) engine is using to display output.
helpviewer_keywords: ["GetWindow","GetWindow method [Windows Controls]","GetWindow method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetWindow method","ITextDocument2.GetWindow","ITextDocument2::GetWindow","controls.itextdocument2_getwindow","tom/ITextDocument2::GetWindow"]
old-location: controls\itextdocument2_getwindow.htm
tech.root: Controls
ms.assetid: 4bf5e644-292e-4847-8dad-71e8ccf86205
ms.date: 12/05/2018
ms.keywords: GetWindow, GetWindow method [Windows Controls], GetWindow method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetWindow method, ITextDocument2.GetWindow, ITextDocument2::GetWindow, controls.itextdocument2_getwindow, tom/ITextDocument2::GetWindow
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextDocument2::GetWindow
 - tom/ITextDocument2::GetWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2.GetWindow
---

# ITextDocument2::GetWindow


## -description

Gets the handle of the window that the Text Object Model (TOM) engine is using to display output.

## -parameters

### -param pHwnd [out, retval]

Type: <b>__int64*</b>

The handle of the window that the TOM engine is using.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A rich edit control doesn't need to own the window that the TOM engine is using. For example, the rich edit control might be windowless. 

The Input Method Editor (IME) needs the handle of the window that is receiving keyboard messages. This method retrieves that handle.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>
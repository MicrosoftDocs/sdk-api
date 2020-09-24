---
UID: NF:tom.ITextRange2.GetProperty
title: ITextRange2::GetProperty (tom.h)
description: Gets the value of a property.
helpviewer_keywords: ["GetProperty","GetProperty method [Windows Controls]","GetProperty method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetProperty method","ITextRange2.GetProperty","ITextRange2::GetProperty","controls.itextrange2_getproperty","tom/ITextRange2::GetProperty"]
old-location: controls\itextrange2_getproperty.htm
tech.root: Controls
ms.assetid: d5e636b9-d02e-46ac-b224-7d1019da44eb
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Windows Controls], GetProperty method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetProperty method, ITextRange2.GetProperty, ITextRange2::GetProperty, controls.itextrange2_getproperty, tom/ITextRange2::GetProperty
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
 - ITextRange2::GetProperty
 - tom/ITextRange2::GetProperty
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
 - ITextRange2.GetProperty
---

# ITextRange2::GetProperty


## -description

Gets the value of a property.

## -parameters

### -param Type [in]

Type: <b>long</b>

The property ID.

### -param pValue [out]

Type: <b>long*</b>

The property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-setproperty">ITextRange2::SetProperty</a>
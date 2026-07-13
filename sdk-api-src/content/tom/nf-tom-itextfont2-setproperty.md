---
UID: NF:tom.ITextFont2.SetProperty
title: ITextFont2::SetProperty (tom.h)
description: Sets the value of the specified property. (ITextFont2.SetProperty)
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetProperty method","ITextFont2.SetProperty","ITextFont2::SetProperty","SetProperty","SetProperty method [Windows Controls]","SetProperty method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setproperty","tom/ITextFont2::SetProperty"]
old-location: controls\itextfont2_setproperty.htm
tech.root: Controls
ms.assetid: c4d35fed-9bf5-431e-96c9-b1d51d51703a
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetProperty method, ITextFont2.SetProperty, ITextFont2::SetProperty, SetProperty, SetProperty method [Windows Controls], SetProperty method [Windows Controls],ITextFont2 interface, controls.itextfont2_setproperty, tom/ITextFont2::SetProperty
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
 - ITextFont2::SetProperty
 - tom/ITextFont2::SetProperty
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
 - ITextFont2.SetProperty
---

# ITextFont2::SetProperty


## -description

Sets the value of the specified property.

## -parameters

### -param Type [in]

Type: <b>long</b>

The ID of the property value to set. Types are defined by TOM. For a list of types, see <a href="/windows/desktop/api/tom/nf-tom-itextfont2-getproperty">ITextFont2::GetProperty</a>.

### -param Value [in]

Type: <b>long</b>

The new property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getproperty">ITextFont2::GetProperty</a>

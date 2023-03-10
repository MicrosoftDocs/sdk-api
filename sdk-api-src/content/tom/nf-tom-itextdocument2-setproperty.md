---
UID: NF:tom.ITextDocument2.SetProperty
title: ITextDocument2::SetProperty (tom.h)
description: Specifies a new value for a property.
helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","SetProperty method","ITextDocument2.SetProperty","ITextDocument2::SetProperty","SetProperty","SetProperty method [Windows Controls]","SetProperty method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_setproperty","tom/ITextDocument2::SetProperty"]
old-location: controls\itextdocument2_setproperty.htm
tech.root: Controls
ms.assetid: 29e70a21-9fab-4fba-9cc4-f1268b005edb
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetProperty method, ITextDocument2.SetProperty, ITextDocument2::SetProperty, SetProperty, SetProperty method [Windows Controls], SetProperty method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setproperty, tom/ITextDocument2::SetProperty
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
 - ITextDocument2::SetProperty
 - tom/ITextDocument2::SetProperty
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
 - ITextDocument2.SetProperty
---

# ITextDocument2::SetProperty


## -description

Specifies a new value for a property.

## -parameters

### -param Type [in]

Type: <b>long</b>

The identifier of the property. For a list of possible property identifiers, see <a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getproperty"> GetProperty</a>.

### -param Value [in]

Type: <b>long</b>

The new property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-getproperty">ITextDocument2:: GetProperty</a>
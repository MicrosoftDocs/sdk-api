---
UID: NF:tom.ITextFont2.GetPropertyInfo
title: ITextFont2::GetPropertyInfo (tom.h)
description: Gets the property type and value of the specified extra property.
helpviewer_keywords: ["GetPropertyInfo","GetPropertyInfo method [Windows Controls]","GetPropertyInfo method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetPropertyInfo method","ITextFont2.GetPropertyInfo","ITextFont2::GetPropertyInfo","controls.itextfont2_getpropertyinfo","tom/ITextFont2::GetPropertyInfo"]
old-location: controls\itextfont2_getpropertyinfo.htm
tech.root: Controls
ms.assetid: bea8f6da-f781-430f-b1cd-c28e11cc61bb
ms.date: 12/05/2018
ms.keywords: GetPropertyInfo, GetPropertyInfo method [Windows Controls], GetPropertyInfo method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetPropertyInfo method, ITextFont2.GetPropertyInfo, ITextFont2::GetPropertyInfo, controls.itextfont2_getpropertyinfo, tom/ITextFont2::GetPropertyInfo
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
 - ITextFont2::GetPropertyInfo
 - tom/ITextFont2::GetPropertyInfo
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
 - ITextFont2.GetPropertyInfo
---

# ITextFont2::GetPropertyInfo


## -description

Gets the property type and value of the specified extra property.

## -parameters

### -param Index [in]

Type: <b>long</b>

The collection index of the extra property.

### -param pType [out]

Type: <b>long*</b>

The property ID.

### -param pValue [out]

Type: <b>long*</b>

The property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>
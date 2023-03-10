---
UID: NF:propsys.PSPropertyBag_ReadStream
title: PSPropertyBag_ReadStream function (propsys.h)
description: Reads the data stream stored in a given property contained in a specified property bag.
helpviewer_keywords: ["PSPropertyBag_ReadStream","PSPropertyBag_ReadStream function [Windows Properties]","properties.PSPropertyBag_ReadStream","propsys/PSPropertyBag_ReadStream","shell.PSPropertyBag_ReadStream","shell_PSPropertyBag_ReadStream"]
old-location: properties\PSPropertyBag_ReadStream.htm
tech.root: properties
ms.assetid: 3D1D8B3E-DD16-4b34-918C-C8478EBF0930
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadStream, PSPropertyBag_ReadStream function [Windows Properties], properties.PSPropertyBag_ReadStream, propsys/PSPropertyBag_ReadStream, shell.PSPropertyBag_ReadStream, shell_PSPropertyBag_ReadStream
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSPropertyBag_ReadStream
 - propsys/PSPropertyBag_ReadStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSPropertyBag_ReadStream
---

# PSPropertyBag_ReadStream function


## -description

Reads the data stream stored in a given property contained in a specified property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object, that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.

### -param value [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

The address of a pointer that, when this function returns successfully, receives the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The caller of the <a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_readstream">PSPropertyBag_ReadStream</a> function needs to call a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object returned by this function.



<a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> and <a href="../ocidl/nn-ocidl-ipersistpropertybag.md">IPersistPropertyBag</a> optimize Save As Text functionality. <b>IPropertyBag</b> and <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a> provide an object with a property bag in which the object can save its properties persistently. <b>IPropertyBag2</b> allows the object to obtain type information for each property: <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768194(v=vs.85)">IPropertyBag2::Read</a> causes one or more properties to be read from the property bag, and <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768195(v=vs.85)">IPropertyBag2::Write</a> causes one or more properties to be saved into the property bag.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_writestream">PSPropertyBag_WriteStream</a>
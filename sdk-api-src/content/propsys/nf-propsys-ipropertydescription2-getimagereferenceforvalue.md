---
UID: NF:propsys.IPropertyDescription2.GetImageReferenceForValue
title: IPropertyDescription2::GetImageReferenceForValue (propsys.h)
description: Gets the image reference associated with a property value.
helpviewer_keywords: ["GetImageReferenceForValue","GetImageReferenceForValue method [Windows Properties]","GetImageReferenceForValue method [Windows Properties]","IPropertyDescription2 interface","IPropertyDescription2 interface [Windows Properties]","GetImageReferenceForValue method","IPropertyDescription2.GetImageReferenceForValue","IPropertyDescription2::GetImageReferenceForValue","properties.IPropertyDescription2_GetImageReferenceForValue","propsys/IPropertyDescription2::GetImageReferenceForValue","shell.IPropertyDescription2_GetImageReferenceForValue","shell_IPropertyDescription2_GetImageReferenceForValue"]
old-location: properties\IPropertyDescription2_GetImageReferenceForValue.htm
tech.root: properties
ms.assetid: d5831e8c-0b98-4cdc-946e-3c359a04caed
ms.date: 12/05/2018
ms.keywords: GetImageReferenceForValue, GetImageReferenceForValue method [Windows Properties], GetImageReferenceForValue method [Windows Properties],IPropertyDescription2 interface, IPropertyDescription2 interface [Windows Properties],GetImageReferenceForValue method, IPropertyDescription2.GetImageReferenceForValue, IPropertyDescription2::GetImageReferenceForValue, properties.IPropertyDescription2_GetImageReferenceForValue, propsys/IPropertyDescription2::GetImageReferenceForValue, shell.IPropertyDescription2_GetImageReferenceForValue, shell_IPropertyDescription2_GetImageReferenceForValue
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IPropertyDescription2::GetImageReferenceForValue
 - propsys/IPropertyDescription2::GetImageReferenceForValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription2.GetImageReferenceForValue
---

# IPropertyDescription2::GetImageReferenceForValue


## -description

Gets the image reference associated with a property value.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

The <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> for which to get an image.

### -param ppszImageRes [out]

Type: <b>LPWSTR*</b>

A pointer to a buffer that receives, when this method returns successfully, a string of the form &lt;dll name&gt;,-&lt;resid&gt; that is suitable to be passed to <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa">PathParseIconLocation</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
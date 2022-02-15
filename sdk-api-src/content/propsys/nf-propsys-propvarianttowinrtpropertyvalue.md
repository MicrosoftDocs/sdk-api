---
UID: NF:propsys.PropVariantToWinRTPropertyValue
title: PropVariantToWinRTPropertyValue function (propsys.h)
description: Extracts data from a PROPVARIANT structure into a Windows Runtime property value.
helpviewer_keywords: ["PropVariantToWinRTPropertyValue","PropVariantToWinRTPropertyValue function [Windows Properties]","properties.propvarianttowinrtpropertyvalue","propsys/PropVariantToWinRTPropertyValue"]
old-location: properties\propvarianttowinrtpropertyvalue.htm
tech.root: properties
ms.assetid: 38DD3673-17FD-4F2A-BA58-A1A9983B92BF
ms.date: 12/05/2018
ms.keywords: PropVariantToWinRTPropertyValue, PropVariantToWinRTPropertyValue function [Windows Properties], properties.propvarianttowinrtpropertyvalue, propsys/PropVariantToWinRTPropertyValue
req.header: propsys.h
req.include-header: Windows.Foundation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: Propsys.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PropVariantToWinRTPropertyValue
 - propsys/PropVariantToWinRTPropertyValue
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
 - PropVariantToWinRTPropertyValue
---

# PropVariantToWinRTPropertyValue function


## -description

Extracts data from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a Windows Runtime property value. Note that in some cases more than one <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> type maps to a single Windows Runtime property type.

## -parameters

### -param propvar [in]

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param riid [in]

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IPropertyValue (defined in Windows.Foundation.h).

### -param ppv [out]

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically an <a href="/uwp/api/Windows.Foundation.IPropertyValue">IPropertyValue</a> pointer. If the call fails, this value is <b>NULL</b>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

We recommend that you use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

## -see-also

<a href="/uwp/api/Windows.Foundation.PropertyValue">PropertyValue class</a>
---
UID: NF:propsys.WinRTPropertyValueToPropVariant
title: WinRTPropertyValueToPropVariant function (propsys.h)
description: Copies the content from a Windows runtime property value to a PROPVARIANT structure.
helpviewer_keywords: ["WinRTPropertyValueToPropVariant","WinRTPropertyValueToPropVariant function [Windows Properties]","properties.winrtpropertyvaluetopropvariant","propsys/WinRTPropertyValueToPropVariant"]
old-location: properties\winrtpropertyvaluetopropvariant.htm
tech.root: properties
ms.assetid: 3D6853B0-0A3F-4ACF-9C93-478688DAE9CF
ms.date: 12/05/2018
ms.keywords: WinRTPropertyValueToPropVariant, WinRTPropertyValueToPropVariant function [Windows Properties], properties.winrtpropertyvaluetopropvariant, propsys/WinRTPropertyValueToPropVariant
req.header: propsys.h
req.include-header: 
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
 - WinRTPropertyValueToPropVariant
 - propsys/WinRTPropertyValueToPropVariant
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
 - WinRTPropertyValueToPropVariant
---

# WinRTPropertyValueToPropVariant function


## -description

Copies the content from a Windows runtime property value to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -parameters

### -param punkPropertyValue [in, optional]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface from which this function can access the contents of a Windows runtime property value by retrieving and using the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">Windows::Foundation::IPropertyValue</a> interface.

### -param ppropvar [out]

Pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. When this function returns, the <b>PROPVARIANT</b> contains the converted info.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-propvarianttowinrtpropertyvalue">PropVariantToWinRTPropertyValue</a>
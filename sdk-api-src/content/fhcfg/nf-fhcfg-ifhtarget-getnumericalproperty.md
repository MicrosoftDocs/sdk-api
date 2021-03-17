---
UID: NF:fhcfg.IFhTarget.GetNumericalProperty
title: IFhTarget::GetNumericalProperty (fhcfg.h)
description: Retrieves a numeric property of the File History backup target that is represented by an IFhTarget interface.
helpviewer_keywords: ["GetNumericalProperty","GetNumericalProperty method [Windows API]","GetNumericalProperty method [Windows API]","IFhTarget interface","IFhTarget interface [Windows API]","GetNumericalProperty method","IFhTarget.GetNumericalProperty","IFhTarget::GetNumericalProperty","fhcfg/IFhTarget::GetNumericalProperty","winprog.ifhtarget_getnumericalproperty"]
old-location: winprog\ifhtarget_getnumericalproperty.htm
tech.root: winprog
ms.assetid: 3FA2F3AB-A406-4F19-AA5A-0D5596F1BF2C
ms.date: 12/05/2018
ms.keywords: GetNumericalProperty, GetNumericalProperty method [Windows API], GetNumericalProperty method [Windows API],IFhTarget interface, IFhTarget interface [Windows API],GetNumericalProperty method, IFhTarget.GetNumericalProperty, IFhTarget::GetNumericalProperty, fhcfg/IFhTarget::GetNumericalProperty, winprog.ifhtarget_getnumericalproperty
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - IFhTarget::GetNumericalProperty
 - fhcfg/IFhTarget::GetNumericalProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhTarget.GetNumericalProperty
---

# IFhTarget::GetNumericalProperty


## -description

Retrieves a numeric property of the File History backup target that is represented by an <a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhtarget">IFhTarget</a> interface.

> [!NOTE] 
> **IFhTarget** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param PropertyType [in]

Specifies the numeric property. See the <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_target_property_type">FH_TARGET_PROPERTY_TYPE</a> enumeration for a list of possible numeric properties.

### -param PropertyValue [out]

Receives the value of the numeric property.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.

## -remarks

The <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_target_property_type">FH_TARGET_PROPERTY_TYPE</a> enumeration defines property types for string properties and numeric properties. However, the <b>IFhTarget::GetNumericalProperty</b> method can only be used to retrieve numeric properties. String properties must be retrieved by  calling the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhtarget-getstringproperty">IFhTarget::GetStringProperty</a> method.

## -see-also

<a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_target_property_type">FH_TARGET_PROPERTY_TYPE</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhtarget">IFhTarget</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhtarget-getstringproperty">IFhTarget::GetStringProperty</a>
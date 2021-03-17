---
UID: NF:fhcfg.IFhTarget.GetStringProperty
title: IFhTarget::GetStringProperty (fhcfg.h)
description: Retrieves a string property of the File History backup target that is represented by an IFhTarget interface.
helpviewer_keywords: ["GetStringProperty","GetStringProperty method [Windows API]","GetStringProperty method [Windows API]","IFhTarget interface","IFhTarget interface [Windows API]","GetStringProperty method","IFhTarget.GetStringProperty","IFhTarget::GetStringProperty","fhcfg/IFhTarget::GetStringProperty","winprog.ifhtarget_getstringproperty"]
old-location: winprog\ifhtarget_getstringproperty.htm
tech.root: winprog
ms.assetid: DC5FE023-FA6E-4B97-AD9D-830975A17159
ms.date: 12/05/2018
ms.keywords: GetStringProperty, GetStringProperty method [Windows API], GetStringProperty method [Windows API],IFhTarget interface, IFhTarget interface [Windows API],GetStringProperty method, IFhTarget.GetStringProperty, IFhTarget::GetStringProperty, fhcfg/IFhTarget::GetStringProperty, winprog.ifhtarget_getstringproperty
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
 - IFhTarget::GetStringProperty
 - fhcfg/IFhTarget::GetStringProperty
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
 - IFhTarget.GetStringProperty
---

# IFhTarget::GetStringProperty


## -description

Retrieves a string property of the File History backup target that is represented by an <a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhtarget">IFhTarget</a> interface.

> [!NOTE] 
> **IFhTarget** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param PropertyType [in]

Specifies the string property. See the <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_target_property_type">FH_TARGET_PROPERTY_TYPE</a> enumeration for the list of possible string property types.

### -param PropertyValue [out]

This parameter must be <b>NULL</b> on input. On output, it receives a pointer to a string that contains the string property. This string is allocated by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. You must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the string when it is no longer needed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.

## -remarks

The <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_target_property_type">FH_TARGET_PROPERTY_TYPE</a> enumeration defines property types for string properties and numeric properties. However, the <b>IFhTarget::GetStringProperty</b> method can only be used to retrieve string properties. Numeric properties must be retrieved by calling the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhtarget-getnumericalproperty">IFhTarget::GetNumericalProperty</a> method.

## -see-also

<a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_target_property_type">FH_TARGET_PROPERTY_TYPE</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhtarget">IFhTarget</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhtarget-getnumericalproperty">IFhTarget::GetNumericalProperty</a>
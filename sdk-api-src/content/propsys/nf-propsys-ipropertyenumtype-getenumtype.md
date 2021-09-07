---
UID: NF:propsys.IPropertyEnumType.GetEnumType
title: IPropertyEnumType::GetEnumType (propsys.h)
description: Gets an enumeration type from an enumeration information structure.
helpviewer_keywords: ["GetEnumType","GetEnumType method [Windows Properties]","GetEnumType method [Windows Properties]","IPropertyEnumType interface","IPropertyEnumType interface [Windows Properties]","GetEnumType method","IPropertyEnumType.GetEnumType","IPropertyEnumType::GetEnumType","PET_DEFAULTVALUE","PET_DISCRETEVALUE","PET_ENDRANGE","PET_RANGEDVALUE","_shell_IPropertyEnumType_GetEnumType","properties.IPropertyEnumType_GetEnumType","propsys/IPropertyEnumType::GetEnumType","shell.IPropertyEnumType_GetEnumType"]
old-location: properties\IPropertyEnumType_GetEnumType.htm
tech.root: properties
ms.assetid: f73ad824-5605-4c3c-b623-debdebdf5780
ms.date: 12/05/2018
ms.keywords: GetEnumType, GetEnumType method [Windows Properties], GetEnumType method [Windows Properties],IPropertyEnumType interface, IPropertyEnumType interface [Windows Properties],GetEnumType method, IPropertyEnumType.GetEnumType, IPropertyEnumType::GetEnumType, PET_DEFAULTVALUE, PET_DISCRETEVALUE, PET_ENDRANGE, PET_RANGEDVALUE, _shell_IPropertyEnumType_GetEnumType, properties.IPropertyEnumType_GetEnumType, propsys/IPropertyEnumType::GetEnumType, shell.IPropertyEnumType_GetEnumType
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IPropertyEnumType::GetEnumType
 - propsys/IPropertyEnumType::GetEnumType
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
 - IPropertyEnumType.GetEnumType
---

# IPropertyEnumType::GetEnumType


## -description

Gets an enumeration type from an enumeration information structure.

## -parameters

### -param penumtype [out]

Type: <b>PROPENUMTYPE*</b>

When this method returns, contains a pointer to one of the values listed below that indicate the enumeration type.



#### PET_DISCRETEVALUE (0)

Use <a href="/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getdisplaytext">GetDisplayText</a> and either <a href="/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getrangeminvalue">GetRangeMinValue</a> or <a href="/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getrangesetvalue">GetRangeSetValue</a>.



#### PET_RANGEDVALUE (1)

Use <a href="/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getdisplaytext">GetDisplayText</a> and either <a href="/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getrangeminvalue">GetRangeMinValue</a> or <a href="/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getrangesetvalue">GetRangeSetValue</a>.



#### PET_DEFAULTVALUE (2)

Use <a href="/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getdisplaytext">GetDisplayText</a>.



#### PET_ENDRANGE (3)

Use <a href="/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getvalue">GetValue</a> or <a href="/windows/desktop/api/propsys/nf-propsys-ipropertyenumtype-getrangeminvalue">GetRangeMinValue</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For additional information, see <a href="/windows/desktop/properties/propdesc-schema-enumeratedlist">enumeratedList</a>.
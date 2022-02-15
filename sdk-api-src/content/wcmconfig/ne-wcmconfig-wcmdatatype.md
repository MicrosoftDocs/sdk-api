---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0003
title: WcmDataType (wcmconfig.h)
description: Enumerates the data types returned from the ISettingsItem::GetDataType method.
helpviewer_keywords: ["WcmDataType","WcmDataType enumeration [SMI]","dataTypeBoolean","dataTypeByte","dataTypeFlagArray","dataTypeInt16","dataTypeInt32","dataTypeInt64","dataTypeSByte","dataTypeString","dataTypeUInt16","dataTypeUInt32","dataTypeUInt64","smi.wcmdatatype","wcmconfig/WcmDataType","wcmconfig/dataTypeBoolean","wcmconfig/dataTypeByte","wcmconfig/dataTypeFlagArray","wcmconfig/dataTypeInt16","wcmconfig/dataTypeInt32","wcmconfig/dataTypeInt64","wcmconfig/dataTypeSByte","wcmconfig/dataTypeString","wcmconfig/dataTypeUInt16","wcmconfig/dataTypeUInt32","wcmconfig/dataTypeUInt64"]
old-location: smi\wcmdatatype.htm
tech.root: SMI
ms.assetid: 27cf5831-f515-4864-bd40-a9d64f30c92d
ms.date: 12/05/2018
ms.keywords: WcmDataType, WcmDataType enumeration [SMI], dataTypeBoolean, dataTypeByte, dataTypeFlagArray, dataTypeInt16, dataTypeInt32, dataTypeInt64, dataTypeSByte, dataTypeString, dataTypeUInt16, dataTypeUInt32, dataTypeUInt64, smi.wcmdatatype, wcmconfig/WcmDataType, wcmconfig/dataTypeBoolean, wcmconfig/dataTypeByte, wcmconfig/dataTypeFlagArray, wcmconfig/dataTypeInt16, wcmconfig/dataTypeInt32, wcmconfig/dataTypeInt64, wcmconfig/dataTypeSByte, wcmconfig/dataTypeString, wcmconfig/dataTypeUInt16, wcmconfig/dataTypeUInt32, wcmconfig/dataTypeUInt64
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WcmDataType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wcmconfig_0000_0000_0003
 - wcmconfig/__MIDL___MIDL_itf_wcmconfig_0000_0000_0003
 - WcmDataType
 - wcmconfig/WcmDataType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcmConfig.h
api_name:
 - WcmDataType
---

# WcmDataType enumeration


## -description

Enumerates the data types returned from the <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getdatatype">ISettingsItem::GetDataType</a> method. The values correspond appropriately to typical programming types. An exception is the flag value <b>dataTypeFlagArray</b>. This flag may appear combined with <b>dataTypeByte</b> or <b>dataTypeString</b> to indicate xsd:hexBinary or wcm:multiString settings (respectively).

Each of the following constants correspond to a data type.

## -enum-fields

### -field dataTypeByte:1

Corresponds to a byte.

### -field dataTypeSByte:2

Corresponds to a signed byte.

### -field dataTypeUInt16:3

Corresponds to an unsigned 16-bit integer.

### -field dataTypeInt16:4

Corresponds to a 16-bit integer.

### -field dataTypeUInt32:5

Corresponds to an unsigned 32-bit integer.

### -field dataTypeInt32:6

Corresponds to a 32-bit integer.

### -field dataTypeUInt64:7

Corresponds to an unsigned 64-bit integer.

### -field dataTypeInt64:8

Corresponds to a 64-bit integer.

### -field dataTypeBoolean:11

Corresponds to a Boolean.

### -field dataTypeString:12

Corresponds to a string.

### -field dataTypeFlagArray:0x8000

This flag may appear combined with <b>dataTypeByte</b> or <b>dataTypeString</b> to indicate xsd:hexBinary or wcm:multiString settings, respectively.

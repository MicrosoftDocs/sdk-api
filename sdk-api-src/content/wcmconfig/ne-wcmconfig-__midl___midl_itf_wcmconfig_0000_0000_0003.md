---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0003
title: "__MIDL___MIDL_itf_wcmconfig_0000_0000_0003"
author: windows-sdk-content
description: Enumerates the data types returned from the ISettingsItem::GetDataType method.
old-location: smi\wcmdatatype.htm
old-project: smi
ms.assetid: 27cf5831-f515-4864-bd40-a9d64f30c92d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WcmDataType, WcmDataType enumeration [SMI], __MIDL___MIDL_itf_wcmconfig_0000_0000_0003, dataTypeBoolean, dataTypeByte, dataTypeFlagArray, dataTypeInt16, dataTypeInt32, dataTypeInt64, dataTypeSByte, dataTypeString, dataTypeUInt16, dataTypeUInt32, dataTypeUInt64, smi.wcmdatatype, wcmconfig/WcmDataType, wcmconfig/dataTypeBoolean, wcmconfig/dataTypeByte, wcmconfig/dataTypeFlagArray, wcmconfig/dataTypeInt16, wcmconfig/dataTypeInt32, wcmconfig/dataTypeInt64, wcmconfig/dataTypeSByte, wcmconfig/dataTypeString, wcmconfig/dataTypeUInt16, wcmconfig/dataTypeUInt32, wcmconfig/dataTypeUInt64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wcmconfig.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WcmDataType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcmConfig.h
api_name:
 - WcmDataType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# __MIDL___MIDL_itf_wcmconfig_0000_0000_0003 enumeration


## -description


Enumerates the data types returned from the <a href="https://msdn.microsoft.com/6ccb99aa-35d5-4f0b-a4f3-a42c4579bc4a">ISettingsItem::GetDataType</a> method. The values correspond appropriately to typical programming types. An exception is the flag value <b>dataTypeFlagArray</b>. This flag may appear combined with <b>dataTypeByte</b> or <b>dataTypeString</b> to indicate xsd:hexBinary or wcm:multiString settings (respectively).

Each of the following constants correspond to a data type.


## -enum-fields




### -field dataTypeByte

Corresponds to a byte.


### -field dataTypeSByte

Corresponds to a signed byte.


### -field dataTypeUInt16

Corresponds to an unsigned 16-bit integer.


### -field dataTypeInt16

Corresponds to a 16-bit integer.


### -field dataTypeUInt32

Corresponds to an unsigned 32-bit integer.


### -field dataTypeInt32

Corresponds to a 32-bit integer.


### -field dataTypeUInt64

Corresponds to an unsigned 64-bit integer.


### -field dataTypeInt64

Corresponds to a 64-bit integer.


### -field dataTypeBoolean

Corresponds to a Boolean.


### -field dataTypeString

Corresponds to a string.


### -field dataTypeFlagArray

This flag may appear combined with <b>dataTypeByte</b> or <b>dataTypeString</b> to indicate xsd:hexBinary or wcm:multiString settings, respectively. 


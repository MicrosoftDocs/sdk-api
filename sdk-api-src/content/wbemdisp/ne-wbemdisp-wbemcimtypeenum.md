---
UID: NE:wbemdisp.WbemCimtypeEnum
title: WbemCimtypeEnum (wbemdisp.h)
description: Define the valid CIM types of a property value.
helpviewer_keywords: ["WbemCimTypeEnum","WbemCimTypeEnum enumeration [Windows Management Instrumentation]","WbemCimtypeEnum","_hmm_wbemcimtypeenum","wbemCimtypeBoolean","wbemCimtypeChar16","wbemCimtypeDatetime","wbemCimtypeObject","wbemCimtypeReal32","wbemCimtypeReal64","wbemCimtypeReference","wbemCimtypeSint16","wbemCimtypeSint32","wbemCimtypeSint64","wbemCimtypeSint8","wbemCimtypeString","wbemCimtypeUint16","wbemCimtypeUint32","wbemCimtypeUint64","wbemCimtypeUint8","wbemdisp/WbemCimTypeEnum","wbemdisp/wbemCimtypeBoolean","wbemdisp/wbemCimtypeChar16","wbemdisp/wbemCimtypeDatetime","wbemdisp/wbemCimtypeObject","wbemdisp/wbemCimtypeReal32","wbemdisp/wbemCimtypeReal64","wbemdisp/wbemCimtypeReference","wbemdisp/wbemCimtypeSint16","wbemdisp/wbemCimtypeSint32","wbemdisp/wbemCimtypeSint64","wbemdisp/wbemCimtypeSint8","wbemdisp/wbemCimtypeString","wbemdisp/wbemCimtypeUint16","wbemdisp/wbemCimtypeUint32","wbemdisp/wbemCimtypeUint64","wbemdisp/wbemCimtypeUint8","wmi.wbemcimtypeenum"]
old-location: wmi\wbemcimtypeenum.htm
tech.root: wmi
ms.assetid: d9929464-742e-4f6c-b631-a6c191167858
ms.date: 12/05/2018
ms.keywords: WbemCimTypeEnum, WbemCimTypeEnum enumeration [Windows Management Instrumentation], WbemCimtypeEnum, _hmm_wbemcimtypeenum, wbemCimtypeBoolean, wbemCimtypeChar16, wbemCimtypeDatetime, wbemCimtypeObject, wbemCimtypeReal32, wbemCimtypeReal64, wbemCimtypeReference, wbemCimtypeSint16, wbemCimtypeSint32, wbemCimtypeSint64, wbemCimtypeSint8, wbemCimtypeString, wbemCimtypeUint16, wbemCimtypeUint32, wbemCimtypeUint64, wbemCimtypeUint8, wbemdisp/WbemCimTypeEnum, wbemdisp/wbemCimtypeBoolean, wbemdisp/wbemCimtypeChar16, wbemdisp/wbemCimtypeDatetime, wbemdisp/wbemCimtypeObject, wbemdisp/wbemCimtypeReal32, wbemdisp/wbemCimtypeReal64, wbemdisp/wbemCimtypeReference, wbemdisp/wbemCimtypeSint16, wbemdisp/wbemCimtypeSint32, wbemdisp/wbemCimtypeSint64, wbemdisp/wbemCimtypeSint8, wbemdisp/wbemCimtypeString, wbemdisp/wbemCimtypeUint16, wbemdisp/wbemCimtypeUint32, wbemdisp/wbemCimtypeUint64, wbemdisp/wbemCimtypeUint8, wmi.wbemcimtypeenum
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WbemCimtypeEnum
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WbemCimtypeEnum
 - wbemdisp/WbemCimtypeEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemdisp.h
api_name:
 - WbemCimTypeEnum
---

# WbemCimtypeEnum enumeration


## -description

The 
WbemCimtypeEnum constants define the valid CIM types of a property value.

The WMI scripting type library, wbemdisp.tlb, defines these constants. Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use the Windows Script Host (WSH) XML file format. For more information, see 
<a href="/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library">Using the WMI Scripting Type Library</a>.

## -enum-fields

### -field wbemCimtypeSint8:16

Signed 8-bit integer

### -field wbemCimtypeUint8:17

Unsigned 8-bit integer

### -field wbemCimtypeSint16:2

Signed 16-bit integer

### -field wbemCimtypeUint16:18

Unsigned 16-bit integer

### -field wbemCimtypeSint32:3

Signed 32-bit integer

### -field wbemCimtypeUint32:19

Unsigned 32-bit integer

### -field wbemCimtypeSint64:20

Signed 64-bit integer

### -field wbemCimtypeUint64:21

Unsigned 64-bit integer

### -field wbemCimtypeReal32:4

32-bit real number

### -field wbemCimtypeReal64:5

64-bit real number

### -field wbemCimtypeBoolean:11

Boolean value

### -field wbemCimtypeString:8

String

### -field wbemCimtypeDatetime:101

Date/time value

### -field wbemCimtypeReference:102

Reference to a CIM object

### -field wbemCimtypeChar16:103

16-bit character

### -field wbemCimtypeObject:13

CIM object

## -see-also

<a href="/windows/win32/api/wbemcli/ne-wbemcli-cimtype_enumeration">CIMTYPE_ENUMERATION</a>



<a href="/windows/desktop/WmiSdk/scripting-api-constants">Scripting API Constants</a>

---
UID: NE:sdoias._ATTRIBUTESYNTAX
title: ATTRIBUTESYNTAX (sdoias.h)
description: Each value from the ATTRIBUTESYNTAX enumeration type specifies a possible attribute syntax.
helpviewer_keywords: ["ATTRIBUTESYNTAX","ATTRIBUTESYNTAX enumeration [Network Policy Server]","IAS_SYNTAX_BOOLEAN","IAS_SYNTAX_ENUMERATOR","IAS_SYNTAX_INETADDR","IAS_SYNTAX_INETADDR6","IAS_SYNTAX_INTEGER","IAS_SYNTAX_OCTETSTRING","IAS_SYNTAX_PROVIDERSPECIFIC","IAS_SYNTAX_STRING","IAS_SYNTAX_UNSIGNEDINTEGER","IAS_SYNTAX_UTCTIME","_sdo_attributesyntax","nps.SDO_attributesyntax","sdo.attributesyntax","sdoias/ATTRIBUTESYNTAX","sdoias/IAS_SYNTAX_BOOLEAN","sdoias/IAS_SYNTAX_ENUMERATOR","sdoias/IAS_SYNTAX_INETADDR","sdoias/IAS_SYNTAX_INETADDR6","sdoias/IAS_SYNTAX_INTEGER","sdoias/IAS_SYNTAX_OCTETSTRING","sdoias/IAS_SYNTAX_PROVIDERSPECIFIC","sdoias/IAS_SYNTAX_STRING","sdoias/IAS_SYNTAX_UNSIGNEDINTEGER","sdoias/IAS_SYNTAX_UTCTIME"]
old-location: nps\SDO_attributesyntax.htm
tech.root: Nps
ms.assetid: 50d56c43-6552-4bb0-a204-a0cfc3ee7202
ms.date: 12/05/2018
ms.keywords: ATTRIBUTESYNTAX, ATTRIBUTESYNTAX enumeration [Network Policy Server], IAS_SYNTAX_BOOLEAN, IAS_SYNTAX_ENUMERATOR, IAS_SYNTAX_INETADDR, IAS_SYNTAX_INETADDR6, IAS_SYNTAX_INTEGER, IAS_SYNTAX_OCTETSTRING, IAS_SYNTAX_PROVIDERSPECIFIC, IAS_SYNTAX_STRING, IAS_SYNTAX_UNSIGNEDINTEGER, IAS_SYNTAX_UTCTIME, _sdo_attributesyntax, nps.SDO_attributesyntax, sdo.attributesyntax, sdoias/ATTRIBUTESYNTAX, sdoias/IAS_SYNTAX_BOOLEAN, sdoias/IAS_SYNTAX_ENUMERATOR, sdoias/IAS_SYNTAX_INETADDR, sdoias/IAS_SYNTAX_INETADDR6, sdoias/IAS_SYNTAX_INTEGER, sdoias/IAS_SYNTAX_OCTETSTRING, sdoias/IAS_SYNTAX_PROVIDERSPECIFIC, sdoias/IAS_SYNTAX_STRING, sdoias/IAS_SYNTAX_UNSIGNEDINTEGER, sdoias/IAS_SYNTAX_UTCTIME
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ATTRIBUTESYNTAX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ATTRIBUTESYNTAX
 - sdoias/_ATTRIBUTESYNTAX
 - ATTRIBUTESYNTAX
 - sdoias/ATTRIBUTESYNTAX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - ATTRIBUTESYNTAX
---

# ATTRIBUTESYNTAX enumeration


## -description

Each value from the 
<b>ATTRIBUTESYNTAX</b> enumeration type specifies a possible attribute syntax.

## -enum-fields

### -field IAS_SYNTAX_BOOLEAN:1

The attribute is of type Boolean.

### -field IAS_SYNTAX_INTEGER

The attribute is of type integer.

### -field IAS_SYNTAX_ENUMERATOR

The attribute is an enumerator.

### -field IAS_SYNTAX_INETADDR

The attribute is an Internet address.

### -field IAS_SYNTAX_STRING

The attribute is a text string.

### -field IAS_SYNTAX_OCTETSTRING

The attribute is a byte (octet) string.

### -field IAS_SYNTAX_UTCTIME

The attribute is a time in coordinated universal time format.

### -field IAS_SYNTAX_PROVIDERSPECIFIC

The attribute and its type are vendor-specific.

### -field IAS_SYNTAX_UNSIGNEDINTEGER

The attribute is of type unsigned integer.

### -field IAS_SYNTAX_INETADDR6

The attribute is an IPv6 address.

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-attributeinfo">ATTRIBUTEINFO</a>

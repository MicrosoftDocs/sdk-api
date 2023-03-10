---
UID: NS:wtsdefs.__WTS_PROPERTY_VALUE
title: WTS_PROPERTY_VALUE (wtsdefs.h)
description: Contains information about a property value to retrieve from the protocol.
helpviewer_keywords: ["*PWTS_PROPERTY_VALUE","PWRDS_PROPERTY_VALUE","PWRDS_PROPERTY_VALUE structure pointer [Remote Desktop Services]","PWTS_PROPERTY_VALUE","PWTS_PROPERTY_VALUE structure pointer [Remote Desktop Services]","VALUE_TYPE_BINARY","VALUE_TYPE_GUID","VALUE_TYPE_STRING","VALUE_TYPE_ULONG","WRDS_PROPERTY_VALUE","WRDS_PROPERTY_VALUE structure [Remote Desktop Services]","WTS_PROPERTY_VALUE","WTS_PROPERTY_VALUE structure [Remote Desktop Services]","termserv.wts_property_value","wtsdefs/PWRDS_PROPERTY_VALUE","wtsdefs/PWTS_PROPERTY_VALUE","wtsdefs/WRDS_PROPERTY_VALUE","wtsdefs/WTS_PROPERTY_VALUE"]
old-location: termserv\wts_property_value.htm
tech.root: TermServ
ms.assetid: 3a4d18db-ef6a-4a7f-a676-1bc952ecae50
ms.date: 12/05/2018
ms.keywords: '*PWTS_PROPERTY_VALUE, PWRDS_PROPERTY_VALUE, PWRDS_PROPERTY_VALUE structure pointer [Remote Desktop Services], PWTS_PROPERTY_VALUE, PWTS_PROPERTY_VALUE structure pointer [Remote Desktop Services], VALUE_TYPE_BINARY, VALUE_TYPE_GUID, VALUE_TYPE_STRING, VALUE_TYPE_ULONG, WRDS_PROPERTY_VALUE, WRDS_PROPERTY_VALUE structure [Remote Desktop Services], WTS_PROPERTY_VALUE, WTS_PROPERTY_VALUE structure [Remote Desktop Services], termserv.wts_property_value, wtsdefs/PWRDS_PROPERTY_VALUE, wtsdefs/PWTS_PROPERTY_VALUE, wtsdefs/WRDS_PROPERTY_VALUE, wtsdefs/WTS_PROPERTY_VALUE'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __WTS_PROPERTY_VALUE
 - wtsdefs/__WTS_PROPERTY_VALUE
 - PWTS_PROPERTY_VALUE
 - wtsdefs/PWTS_PROPERTY_VALUE
 - WTS_PROPERTY_VALUE
 - wtsdefs/WTS_PROPERTY_VALUE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_PROPERTY_VALUE
---

# WTS_PROPERTY_VALUE structure


## -description

Contains information about a property value to retrieve from the protocol. The <b>WTS_PROPERTY_VALUE</b> structure is used by the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty">QueryProperty</a> method.

## -struct-fields

### -field Type

An integer that specifies which member of the union contains the property value information. This can be one of the following values.



#### VALUE_TYPE_ULONG

The value is contained in the <b>ulVal</b> member.



#### VALUE_TYPE_STRING

The value is contained in the <b>strVal</b> member.



#### VALUE_TYPE_BINARY

The value is contained in the <b>bVal</b> member.



#### VALUE_TYPE_GUID

The value is contained in the <b>guidVal</b> member.

### -field u

A union that contains the property value.

### -field u.ulVal

The value is contained in an integer.

### -field u.strVal

The value is contained in a string.

### -field u.strVal.size

An integer that contains the size of the string pointed to by the <b>pstrVal</b> member.

### -field u.strVal.pstrVal

A pointer to a string that contains the property value.

### -field u.bVal

The value is contained in a byte array.

### -field u.bVal.size

An integer that contains the size of the byte array pointed to by the <b>pbVal</b> member.

### -field u.bVal.pbVal

A pointer to a byte array that contains the property value.

### -field u.guidVal

A GUID that contains the property value.
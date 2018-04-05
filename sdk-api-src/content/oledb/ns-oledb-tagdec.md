---
UID: NS:oledb.tagDEC
title: tagDEC
author: windows-driver-content
description: Represents a decimal data type that provides a sign and scale for a number (as in coordinates.).
old-location: automat\decimal.htm
old-project: automat
ms.assetid: 0b3295be-1ec2-4dd7-9197-cef335f7d8b9
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: DECIMAL, DECIMAL structure [Automation], _oa96_DECIMAL, automat.decimal, oledb/DECIMAL, tagDEC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: oledb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DECIMAL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	OleDb.h
api_name:
-	DECIMAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagDEC structure


## -description


Represents a decimal data type that provides a sign and scale for a number (as in coordinates.)

Decimal variables are stored as 96-bit (12-byte) unsigned integers scaled by a variable power of 10. The power of 10 scaling factor specifies the number of digits to the right of the decimal point, and ranges from 0 to 28.


## -struct-fields




### -field scale

The number of decimal places for the number. Valid values are from 0 to 28. So 12.345 is represented as 12345 with a scale of 3.


### -field sign

Indicates the sign; 0 for positive numbers or DECIMAL_NEG for negative numbers. So -1 is represented as 1 with the DECIMAL_NEG bit set.


### -field Lo32

The low 32 bits of the number.


### -field Mid32

The middle 32 bits of the number.


### -field wReserved

Reserved.


### -field Hi32

The high 32 bits of the number.


#### - Lo64

The low 64 bits of the number. This is an _int64.


#### - signscale

The sign and number of decimal places.


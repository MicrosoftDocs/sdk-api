---
UID: NS:bdamedia._SpanningEventEmmMessage
title: "_SpanningEventEmmMessage"
author: windows-driver-content
description: Contains information about an Entitlement Management Message (EMM). For more information, refer to ARIB STD-B25, Conditional Access System Specifications for Digital Broadcasting. (This resource may not be available in some languages and countries.).
old-location: mstv\spanningeventemmmessage.htm
old-project: mstv
ms.assetid: e362a3b5-db4a-4a58-adf9-d799f83c9f36
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: SpanningEventEmmMessage, SpanningEventEmmMessage structure [Microsoft TV Technologies], _SpanningEventEmmMessage, bdamedia/SpanningEventEmmMessage, mstv.spanningeventemmmessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdamedia.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SpanningEventEmmMessage
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdamedia.h
api_name:
-	SpanningEventEmmMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _SpanningEventEmmMessage structure


## -description


Contains information about an Entitlement Management Message (EMM). For more information, refer to ARIB STD-B25, <i>Conditional Access System Specifications for Digital Broadcasting</i>. (This resource may not be available in some languages 

and countries.)


## -struct-fields




### -field bCAbroadcasterGroupId

The value of the ca_broadcaster_group_ID field from the Condition Access (CA) service descriptor.


### -field bMessageControl

The value of the message_control field from the CA service descriptor.


### -field wServiceId

The service ID for the network.


### -field wTableIdExtension

The table ID extension. If this value is zero, the remaining structure members are ignored.


### -field bDeletionStatus

The value of the deletion_status field.


### -field bDisplayingDuration1

The value of the displaying_duration1 field.


### -field bDisplayingDuration2

The value of the displaying_duration2 field.


### -field bDisplayingDuration3

The value of the displaying_duration3 field.


### -field bDisplayingCycle

The value of the displaying_cycle field.,


### -field bFormatVersion

The value of the format_version field.


### -field bDisplayPosition

The display position. 


### -field wMessageLength

The number of bytes of data in the <b>szMessageArea</b> array.


### -field szMessageArea

The contents of the message. This array might be larger than the size given in the structure declaration. Use the value of <b>szMessageArea</b> to determine the size.


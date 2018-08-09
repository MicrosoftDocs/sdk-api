---
UID: NS:wsdxml._WSD_DURATION
title: "_WSD_DURATION"
author: windows-sdk-content
description: Represents a length of time.
old-location: ncd\wsd_duration_struct.htm
old-project: wsdapi
ms.assetid: 43d4d0c5-509a-46c4-bdf6-24c3307fb811
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSD_DURATION, WSD_DURATION structure, _WSD_DURATION, ncd.wsd_duration_struct, wsdxml/WSD_DURATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdxml.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdXml.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_DURATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdXml.h
api_name:
 - WSD_DURATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_DURATION structure


## -description


Represents a length of time.


## -struct-fields




### -field isPositive

This parameter is <b>TRUE</b> if the entire duration is positive.


### -field year

The year value. This number is a value between 0 and max(ULONG).


### -field month

The month value. This number is a value between 0 and max(ULONG).


### -field day

The day value. This number is a value between 0 and max(ULONG).


### -field hour

The hour value. This number is a value between 0 and max(ULONG).


### -field minute

The minute value. This number is a value between 0 and max(ULONG).


### -field second

The second value. This number is a value between 0 and max(ULONG).


### -field millisecond

The millisecond value (0-999).


## -remarks



If any numeric member has a value of 0, then the member and its value is not included in the XML output when the structure is converted to XML.




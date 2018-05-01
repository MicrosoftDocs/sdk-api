---
UID: NS:dhcpcsdk._DHCPCAPI_CLASSID
title: "_DHCPCAPI_CLASSID"
author: windows-driver-content
description: The DHCPCAPI_CLASSID structure defines a client Class ID.
old-location: dhcp\dhcpcapi_classid.htm
old-project: DHCP
ms.assetid: ef1167cb-fcfb-4de3-8b3c-d306f69472f3
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: "*LPDHCPCAPI_CLASSID, *LPDHCPCAPI_CLASSID structure [DHCP], *PDHCPCAPI_CLASSID, *PDHCPCAPI_CLASSID structure [DHCP], DHCPCAPI_CLASSID, DHCPCAPI_CLASSID structure [DHCP], _DHCPCAPI_CLASSID, dhcp.dhcpcapi_classid, dhcpcsdk/*LPDHCPCAPI_CLASSID, dhcpcsdk/*PDHCPCAPI_CLASSID, dhcpcsdk/DHCPCAPI_CLASSID"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpcsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DHCPCAPI_CLASSID, *PDHCPCAPI_CLASSID, *LPDHCPCAPI_CLASSID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpcsdk.h
api_name:
-	DHCPCAPI_CLASSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCPCAPI_CLASSID structure


## -description


The <b>DHCPCAPI_CLASSID</b> structure defines a client Class ID.


## -struct-fields




### -field Flags

Reserved. Must be set to zero.


### -field Data

Class ID binary data.


### -field nBytesData

Size of <b>Data</b>, in bytes.


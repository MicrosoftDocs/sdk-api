---
UID: NS:dhcpv6csdk._DHCPV6CAPI_CLASSID
title: "_DHCPV6CAPI_CLASSID"
author: windows-sdk-content
description: Defines an IPv6 client class ID.
old-location: dhcp\dhcpv6capi_classid.htm
old-project: DHCP
ms.assetid: 90dbc386-02d9-4631-8af3-edd34537fefc
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCPV6CAPI_CLASSID, *PDHCPV6CAPI_CLASSID, DHCPV6CAPI_CLASSID, DHCPV6CAPI_CLASSID structure [DHCP], LPDHCPV6CAPI_CLASSID, LPDHCPV6CAPI_CLASSID structure pointer [DHCP], PDHCPV6CAPI_CLASSID, PDHCPV6CAPI_CLASSID structure pointer [DHCP], _DHCPV6CAPI_CLASSID, dhcp.dhcpv6capi_classid, dhcpv6csdk/DHCPV6CAPI_CLASSID, dhcpv6csdk/LPDHCPV6CAPI_CLASSID, dhcpv6csdk/PDHCPV6CAPI_CLASSID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dhcpv6csdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DHCPV6CAPI_CLASSID, *PDHCPV6CAPI_CLASSID, *LPDHCPV6CAPI_CLASSID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpv6csdk.h
api_name:
-	DHCPV6CAPI_CLASSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCPV6CAPI_CLASSID structure


## -description


The <b>DHCPV6CAPI_CLASSID</b> structure defines an IPv6 client class ID.


## -struct-fields




### -field Flags

Reserved for future use.  Must be set to 0.


### -field Data.size_is

 


### -field Data.size_is.nBytesData

 


### -field Data

Class ID binary data.


### -field nBytesData

Size of <b>Data</b>, in bytes.


---
UID: NE:portabledevice.tagWPD_PARAMETER_USAGE_TYPES
title: tagWPD_PARAMETER_USAGE_TYPES
author: windows-driver-content
description: The WPD_PARAMETER_USAGE_TYPES enumeration type describes how a method parameter is used in a given method.
old-location: wpdsdk\wpd_parameter_usage_types.htm
old-project: wpd_sdk
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPD_PARAMETER_USAGE_IN, WPD_PARAMETER_USAGE_INOUT, WPD_PARAMETER_USAGE_OUT, WPD_PARAMETER_USAGE_RETURN, WPD_PARAMETER_USAGE_TYPES, WPD_PARAMETER_USAGE_TYPES enumeration [Windows Portable Devices SDK], portabledevice/WPD_PARAMETER_USAGE_IN, portabledevice/WPD_PARAMETER_USAGE_INOUT, portabledevice/WPD_PARAMETER_USAGE_OUT, portabledevice/WPD_PARAMETER_USAGE_RETURN, portabledevice/WPD_PARAMETER_USAGE_TYPES, tagWPD_PARAMETER_USAGE_TYPES, wpdsdk.wpd_parameter_usage_types
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: portabledevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WPD_PARAMETER_USAGE_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	WPD_PARAMETER_USAGE_TYPES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagWPD_PARAMETER_USAGE_TYPES enumeration


## -description


The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597896">WPD_PARAMETER_USAGE_TYPES</a> enumeration type describes how a method parameter is used in a given method.


## -enum-fields




### -field WPD_PARAMETER_USAGE_RETURN

The parameter receives the return value, if specified by the method.


### -field WPD_PARAMETER_USAGE_IN

The parameter contains an input value before the method is called.


### -field WPD_PARAMETER_USAGE_OUT

The parameter contains an output value when the method returns.


### -field WPD_PARAMETER_USAGE_INOUT

The parameter contains an input value before the method is called and an output value when it returns.


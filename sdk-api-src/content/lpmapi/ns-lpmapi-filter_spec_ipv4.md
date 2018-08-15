---
UID: NS:lpmapi.Filter_Spec_IPv4
title: Filter_Spec_IPv4
author: windows-sdk-content
description: The Filter_Spec_IPv4 structure contains information about an IPv4 FILTERSPEC.
old-location: qos\filter_spec_ipv4.htm
old-project: qos
ms.assetid: b17a45b2-e50b-4ec2-9f1c-e1ab80ce572e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Filter_Spec_IPv4, Filter_Spec_IPv4 structure [QOS], lpmapi/Filter_Spec_IPv4, qos.filter_spec_ipv4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: Filter_Spec_IPv4
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - Filter_Spec_IPv4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# Filter_Spec_IPv4 structure


## -description


The 
<b>Filter_Spec_IPv4</b> structure contains information about an IPv4 FILTERSPEC.


## -struct-fields




### -field filt_ipaddr

IP address of the source address, in the form of an <a href="https://msdn.microsoft.com/fc41a2d1-ea6e-41bb-b2c8-531ac8b5434c">in_addr</a> structure.


### -field filt_unused

Reserved. Do not use.


### -field filt_port

TCP port for the source.


## -see-also




<a href="https://msdn.microsoft.com/fc41a2d1-ea6e-41bb-b2c8-531ac8b5434c">in_addr</a>
 

 


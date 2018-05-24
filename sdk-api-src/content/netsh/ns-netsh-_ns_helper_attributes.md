---
UID: NS:netsh._NS_HELPER_ATTRIBUTES
title: "_NS_HELPER_ATTRIBUTES"
author: windows-driver-content
description: Provides attributes of a helper.
old-location: netshell\ns_helper_attributes.htm
old-project: NetShell
ms.assetid: b2a3ae40-4aaa-41b2-965c-1467a07ab2de
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*PNS_HELPER_ATTRIBUTES, NS_HELPER_ATTRIBUTES, NS_HELPER_ATTRIBUTES structure [NetShell], PNS_HELPER_ATTRIBUTES, PNS_HELPER_ATTRIBUTES structure pointer [NetShell], _NS_HELPER_ATTRIBUTES, _netsh_ns_helper_attributes, netsh/NS_HELPER_ATTRIBUTES, netsh/PNS_HELPER_ATTRIBUTES, netshell.ns_helper_attributes"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: netsh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NS_HELPER_ATTRIBUTES, *PNS_HELPER_ATTRIBUTES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Netsh.h
api_name:
-	NS_HELPER_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _NS_HELPER_ATTRIBUTES structure


## -description


The 
<b>NS_HELPER_ATTRIBUTES</b> structure provides attributes of a helper.


## -struct-fields




### -field dwVersion

The version of the helper.


### -field dwReserved

Reserved. Must be zero.


### -field _ullAlign

 


### -field guidHelper

The GUID of the helper.


### -field pfnStart

A pointer to the 
<a href="https://msdn.microsoft.com/0060feb9-3072-4a1c-9d25-4c304f60d42d">NS_HELPER_START_FN</a> entry point (the start function) of the helper.


### -field pfnStop

A pointer to the 
<a href="https://msdn.microsoft.com/a56c11e6-5314-43eb-9960-55987395112f">NS_HELPER_STOP_FN</a> entry point (the stop function) of the helper. Set to null if no stop function is implemented.


## -see-also




<a href="https://msdn.microsoft.com/0060feb9-3072-4a1c-9d25-4c304f60d42d">NS_HELPER_START_FN</a>



<a href="https://msdn.microsoft.com/a56c11e6-5314-43eb-9960-55987395112f">NS_HELPER_STOP_FN</a>
 

 


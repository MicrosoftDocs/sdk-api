---
UID: NC:rtmv2._ENTITY_METHOD
title: "_ENTITY_METHOD"
author: windows-driver-content
description: The RTM_ENTITY_EXPORT_METHOD callback is the prototype for any method exported by a client.
old-location: rras\rtm_entity_export_method.htm
old-project: RRAS
ms.assetid: bf564898-e540-458b-861c-0f57082d40a1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: RTM_ENTITY_EXPORT_METHOD, RTM_ENTITY_EXPORT_METHOD callback function [RAS], RTM_ENTITY_EXPORT_METHOD callback function pointer [RAS], _ENTITY_METHOD, _rtmv2ref_rtm_entity_export_method, rras.rtm_entity_export_method, rtmv2/RTM_ENTITY_EXPORT_METHOD
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: ProxyFileInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Rtmv2.h
api_name:
-	RTM_ENTITY_EXPORT_METHOD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _ENTITY_METHOD callback


## -description


The 
<b>RTM_ENTITY_EXPORT_METHOD</b> callback is the prototype for any method exported by a client.


## -parameters




### -param CallerHandle

Handle to the calling client.


### -param CalleeHandle

Handle to the client being called.


### -param *Input

Handle to the method to be invoked. Contains an input buffer.


### -param *Output

An array of 
<a href="https://msdn.microsoft.com/9ec05355-a912-4ed0-ace9-8823d333bab5">RTM_ENTITY_METHOD_OUTPUT</a> structures. Each structure consists of a (method identifier, correct output) tuple.


## -returns



This callback function does not return a value.




## -remarks



Methods can be exported when a client registers. Other clients, such as routing protocols, can invoke these methods to obtain client-specific information. For example, BGP can use a method to obtain OSFP information.




## -see-also




<a href="https://msdn.microsoft.com/1f900e85-c522-47c9-bfc8-5a1c1d01ab78">RTM_ENTITY_METHOD_INPUT</a>



<a href="https://msdn.microsoft.com/9ec05355-a912-4ed0-ace9-8823d333bab5">RTM_ENTITY_METHOD_OUTPUT</a>
 

 


---
UID: NC:rtmv2._ENTITY_METHOD
title: _ENTITY_METHOD (rtmv2.h)
description: The RTM_ENTITY_EXPORT_METHOD callback is the prototype for any method exported by a client.
helpviewer_keywords: ["RTM_ENTITY_EXPORT_METHOD","RTM_ENTITY_EXPORT_METHOD callback function [RAS]","RTM_ENTITY_EXPORT_METHOD callback function pointer [RAS]","_ENTITY_METHOD","_ENTITY_METHOD callback","_rtmv2ref_rtm_entity_export_method","rras.rtm_entity_export_method","rtmv2/RTM_ENTITY_EXPORT_METHOD"]
old-location: rras\rtm_entity_export_method.htm
tech.root: RRAS
ms.assetid: bf564898-e540-458b-861c-0f57082d40a1
ms.date: 12/05/2018
ms.keywords: RTM_ENTITY_EXPORT_METHOD, RTM_ENTITY_EXPORT_METHOD callback function [RAS], RTM_ENTITY_EXPORT_METHOD callback function pointer [RAS], _ENTITY_METHOD, _ENTITY_METHOD callback, _rtmv2ref_rtm_entity_export_method, rras.rtm_entity_export_method, rtmv2/RTM_ENTITY_EXPORT_METHOD
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENTITY_METHOD
 - rtmv2/_ENTITY_METHOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Rtmv2.h
api_name:
 - RTM_ENTITY_EXPORT_METHOD
---

# _ENTITY_METHOD callback function


## -description

The 
<b>RTM_ENTITY_EXPORT_METHOD</b> callback is the prototype for any method exported by a client.

## -parameters

### -param CallerHandle

Handle to the calling client.

### -param CalleeHandle

Handle to the client being called.

### -param Input

Handle to the method to be invoked. Contains an input buffer.

### -param Output

An array of 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_method_output">RTM_ENTITY_METHOD_OUTPUT</a> structures. Each structure consists of a (method identifier, correct output) tuple.

## -remarks

Methods can be exported when a client registers. Other clients, such as routing protocols, can invoke these methods to obtain client-specific information. For example, BGP can use a method to obtain OSFP information.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_method_input">RTM_ENTITY_METHOD_INPUT</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_method_output">RTM_ENTITY_METHOD_OUTPUT</a>

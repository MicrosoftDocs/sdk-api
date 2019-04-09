---
UID: NE:mfidl._MF_CONNECT_METHOD
title: MF_CONNECT_METHOD (mfidl.h)
author: windows-sdk-content
description: Specifies how the topology loader connects a topology node.
old-location: mf\mf_connect_method.htm
tech.root: medfound
ms.assetid: 881045bf-ea3b-46e2-aae0-b26e35882da1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 881045bf-ea3b-46e2-aae0-b26e35882da1, MF_CONNECT_ALLOW_CONVERTER, MF_CONNECT_ALLOW_DECODER, MF_CONNECT_AS_OPTIONAL, MF_CONNECT_AS_OPTIONAL_BRANCH, MF_CONNECT_DIRECT, MF_CONNECT_METHOD, MF_CONNECT_METHOD enumeration [Media Foundation], MF_CONNECT_RESOLVE_INDEPENDENT_OUTPUTTYPES, mf.mf_connect_method, mfidl/MF_CONNECT_ALLOW_CONVERTER, mfidl/MF_CONNECT_ALLOW_DECODER, mfidl/MF_CONNECT_AS_OPTIONAL, mfidl/MF_CONNECT_AS_OPTIONAL_BRANCH, mfidl/MF_CONNECT_DIRECT, mfidl/MF_CONNECT_METHOD, mfidl/MF_CONNECT_RESOLVE_INDEPENDENT_OUTPUTTYPES
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_CONNECT_METHOD
product: Windows
targetos: Windows
req.typenames: MF_CONNECT_METHOD
req.redist: 
---

# MF_CONNECT_METHOD enumeration


## -description


Specifies how the topology loader connects a topology node. This enumeration is used with the <a href="https://msdn.microsoft.com/8d70e1af-607b-47c3-9808-091c95fd05b7">MF_TOPONODE_CONNECT_METHOD</a> attribute.
        
      


## -enum-fields




### -field MF_CONNECT_DIRECT

Connect the node directly to its upstream neighbor. Fail otherwise.
          


### -field MF_CONNECT_ALLOW_CONVERTER

Add a converter transform upstream from this node, if needed to complete the connection. Converter transforms include color-space converters for video, and audio resamplers for audio.
          


### -field MF_CONNECT_ALLOW_DECODER

Add a decoder transform upstream upstream from this node, if needed to complete the connection. The numeric value of this flag includes the <b>MF_CONNECT_ALLOW_CONVERTER</b> flag. Therefore, setting the <b>MF_CONNECT_ALLOW_DECODER</b> flag sets the <b>MF_CONNECT_ALLOW_CONVERTER</b> flag as well.
          


### -field MF_CONNECT_RESOLVE_INDEPENDENT_OUTPUTTYPES

Controls the order in which the topology loader attempts to  
            use different output types from this node. Currently, this flag applies only to source nodes. For more information, see <a href="https://msdn.microsoft.com/2675ef16-2018-47e8-bb22-2fc0d62e6681">MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES</a>. 

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MF_CONNECT_AS_OPTIONAL

This node is optional. If the topology loader cannot connect this node, it will skip the node and continue.
          


### -field MF_CONNECT_AS_OPTIONAL_BRANCH

The entire topology branch starting at this node is optional. If the topology loader cannot resolve this branch, it will skip the branch and continue.
          


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 


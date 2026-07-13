---
UID: NE:mfidl._MF_CONNECT_METHOD
title: MF_CONNECT_METHOD (mfidl.h)
description: Specifies how the topology loader connects a topology node.
helpviewer_keywords: ["881045bf-ea3b-46e2-aae0-b26e35882da1","MF_CONNECT_ALLOW_CONVERTER","MF_CONNECT_ALLOW_DECODER","MF_CONNECT_AS_OPTIONAL","MF_CONNECT_AS_OPTIONAL_BRANCH","MF_CONNECT_DIRECT","MF_CONNECT_METHOD","MF_CONNECT_METHOD enumeration [Media Foundation]","MF_CONNECT_RESOLVE_INDEPENDENT_OUTPUTTYPES","mf.mf_connect_method","mfidl/MF_CONNECT_ALLOW_CONVERTER","mfidl/MF_CONNECT_ALLOW_DECODER","mfidl/MF_CONNECT_AS_OPTIONAL","mfidl/MF_CONNECT_AS_OPTIONAL_BRANCH","mfidl/MF_CONNECT_DIRECT","mfidl/MF_CONNECT_METHOD","mfidl/MF_CONNECT_RESOLVE_INDEPENDENT_OUTPUTTYPES"]
old-location: mf\mf_connect_method.htm
tech.root: mf
ms.assetid: 881045bf-ea3b-46e2-aae0-b26e35882da1
ms.date: 12/05/2018
ms.keywords: 881045bf-ea3b-46e2-aae0-b26e35882da1, MF_CONNECT_ALLOW_CONVERTER, MF_CONNECT_ALLOW_DECODER, MF_CONNECT_AS_OPTIONAL, MF_CONNECT_AS_OPTIONAL_BRANCH, MF_CONNECT_DIRECT, MF_CONNECT_METHOD, MF_CONNECT_METHOD enumeration [Media Foundation], MF_CONNECT_RESOLVE_INDEPENDENT_OUTPUTTYPES, mf.mf_connect_method, mfidl/MF_CONNECT_ALLOW_CONVERTER, mfidl/MF_CONNECT_ALLOW_DECODER, mfidl/MF_CONNECT_AS_OPTIONAL, mfidl/MF_CONNECT_AS_OPTIONAL_BRANCH, mfidl/MF_CONNECT_DIRECT, mfidl/MF_CONNECT_METHOD, mfidl/MF_CONNECT_RESOLVE_INDEPENDENT_OUTPUTTYPES
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
targetos: Windows
req.typenames: MF_CONNECT_METHOD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_CONNECT_METHOD
 - mfidl/_MF_CONNECT_METHOD
 - MF_CONNECT_METHOD
 - mfidl/MF_CONNECT_METHOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_CONNECT_METHOD
---

# MF_CONNECT_METHOD enumeration


## -description

Specifies how the topology loader connects a topology node. This enumeration is used with the <a href="/windows/desktop/medfound/mf-toponode-connect-method-attribute">MF_TOPONODE_CONNECT_METHOD</a> attribute.

## -enum-fields

### -field MF_CONNECT_DIRECT:0

Connect the node directly to its upstream neighbor. Fail otherwise.

### -field MF_CONNECT_ALLOW_CONVERTER:0x1

Add a converter transform upstream from this node, if needed to complete the connection. Converter transforms include color-space converters for video, and audio resamplers for audio.

### -field MF_CONNECT_ALLOW_DECODER:0x3

Add a decoder transform upstream upstream from this node, if needed to complete the connection. The numeric value of this flag includes the <b>MF_CONNECT_ALLOW_CONVERTER</b> flag. Therefore, setting the <b>MF_CONNECT_ALLOW_DECODER</b> flag sets the <b>MF_CONNECT_ALLOW_CONVERTER</b> flag as well.

### -field MF_CONNECT_RESOLVE_INDEPENDENT_OUTPUTTYPES:0x4

Controls the order in which the topology loader attempts to  
            use different output types from this node. Currently, this flag applies only to source nodes. For more information, see <a href="/windows/desktop/medfound/mf-topology-enumerate-source-types">MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES</a>. 

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MF_CONNECT_AS_OPTIONAL:0x10000

This node is optional. If the topology loader cannot connect this node, it will skip the node and continue.

### -field MF_CONNECT_AS_OPTIONAL_BRANCH:0x20000

The entire topology branch starting at this node is optional. If the topology loader cannot resolve this branch, it will skip the branch and continue.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>

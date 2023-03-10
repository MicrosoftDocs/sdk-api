---
UID: NN:tapi3.ITAllocatorProperties
title: ITAllocatorProperties (tapi3.h)
description: The ITAllocatorProperties interface (tapi3.h) exposes the buffer allocator properties of the Media Streaming Terminal (MST) to an end-user or server application. 
helpviewer_keywords: ["ITAllocatorProperties","ITAllocatorProperties interface [TAPI 2.2]","ITAllocatorProperties interface [TAPI 2.2]","described","_tapi3_itallocatorproperties","tapi3.itallocatorproperties","tapi3ds/ITAllocatorProperties"]
old-location: tapi3\itallocatorproperties.htm
tech.root: tapi3
ms.assetid: a0facf08-1b03-415b-b97e-3fda5a164b89
ms.date: 08/09/2022
ms.keywords: ITAllocatorProperties, ITAllocatorProperties interface [TAPI 2.2], ITAllocatorProperties interface [TAPI 2.2],described, _tapi3_itallocatorproperties, tapi3.itallocatorproperties, tapi3ds/ITAllocatorProperties
req.header: tapi3.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAllocatorProperties
 - tapi3/ITAllocatorProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAllocatorProperties
---

# ITAllocatorProperties interface


## -description

The 
<b>ITAllocatorProperties</b> interface exposes the buffer allocator properties of the Media Streaming Terminal (MST) to an end-user or server application. An application needs to tune the sample size for a particular protocol. The decision concerning appropriate properties is highly implementation dependent.

This interface is exposed on the 
<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a> by the associated Media Service Provider. If it exists, a <b>QueryInterface</b> on any Terminal interface, such as 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>, can be used to obtain an 
<b>ITAllocatorProperties</b> pointer.

## -inheritance

The <b>ITAllocatorProperties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITAllocatorProperties</b> also has these types of members:


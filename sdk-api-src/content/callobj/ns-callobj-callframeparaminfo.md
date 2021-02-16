---
UID: NS:callobj.__MIDL_ICallFrame_0002
title: CALLFRAMEPARAMINFO (callobj.h)
description: Provides information about the parameter on the stack.
helpviewer_keywords: ["CALLFRAMEPARAMINFO","CALLFRAMEPARAMINFO structure [COM]","callobj/CALLFRAMEPARAMINFO","com.callframeparaminfo"]
old-location: com\callframeparaminfo.htm
tech.root: com
ms.assetid: 0f3a1e81-c8b6-4141-8712-c600b30a2779
ms.date: 12/05/2018
ms.keywords: CALLFRAMEPARAMINFO, CALLFRAMEPARAMINFO structure [COM], callobj/CALLFRAMEPARAMINFO, com.callframeparaminfo
req.header: callobj.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CALLFRAMEPARAMINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_ICallFrame_0002
 - callobj/__MIDL_ICallFrame_0002
 - CALLFRAMEPARAMINFO
 - callobj/CALLFRAMEPARAMINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - callobj.h
api_name:
 - CALLFRAMEPARAMINFO
---

# CALLFRAMEPARAMINFO structure


## -description

Provides information about the parameter on the stack.

## -struct-fields

### -field fIn

<b>TRUE</b> if this is an [in] parameter; otherwise, <b>FALSE</b>.

### -field fOut

<b>TRUE</b> if this is an [out] parameter; otherwise, <b>FALSE</b>.

### -field stackOffset

Represents the offset in bytes from the stack location of the frame to the start of the parameter.

### -field cbParam

Represents the size in bytes occupied by the parameter on the stack.

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>
---
UID: NS:callobj.__MIDL_ICallFrame_0001
title: CALLFRAMEINFO (callobj.h)
description: Provides information about a call frame such as the method in the call frame, if it has in, out, or in/out parameters, the number of [in], [out], or [in, out] interfaces, the interface ID, the number of methods in the interface and the number of parameters in this method.
helpviewer_keywords: ["CALLFRAMEINFO","CALLFRAMEINFO structure [COM]","callobj/CALLFRAMEINFO","com.callframeinfo"]
old-location: com\callframeinfo.htm
tech.root: com
ms.assetid: 3d490c8b-d254-458b-b355-39c3942ddc5e
ms.date: 12/05/2018
ms.keywords: CALLFRAMEINFO, CALLFRAMEINFO structure [COM], callobj/CALLFRAMEINFO, com.callframeinfo
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
req.typenames: CALLFRAMEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_ICallFrame_0001
 - callobj/__MIDL_ICallFrame_0001
 - CALLFRAMEINFO
 - callobj/CALLFRAMEINFO
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
 - CALLFRAMEINFO
---

# CALLFRAMEINFO structure


## -description

Provides information about a call frame such as the method in the call frame, if it has in, out, or in/out parameters, the number of [in], [out], or [in, out] interfaces, the interface ID, the number of methods in the interface and the number of parameters in this method.

## -struct-fields

### -field iMethod

The method number within the interface in question.

### -field fHasInValues

<b>TRUE</b> if there are any [in] parameters in the method; otherwise, <b>FALSE</b>.

### -field fHasInOutValues

<b>TRUE</b> if there are any [in, out] parameters in the method; otherwise, <b>FALSE</b>.

### -field fHasOutValues

<b>TRUE</b> if there are any out parameters other than <b>HRESULT</b> or <b>void</b> return values in the method; otherwise, <b>FALSE</b>.

### -field fDerivesFromIDispatch

<b>TRUE</b> if the interface is derived from <b>IDispatch</b>; otherwise, <b>FALSE</b>.

### -field cInInterfacesMax

If this parameter has a value greater or equal to 0, then the value is an absolute upper bound on the number [in] interfaces. If this parameter is less than 0, then the method may have an unbounded number of [in] interfaces. If this parameter is equal to 0, then there are no [in] interfaces.

### -field cInOutInterfacesMax

If this parameter has a value greater or equal to 0, then the value is an absolute upper bound on the number [in, out] interfaces. If this parameter is less than 0, then the method may have an unbounded number of [in, out] interfaces. If this parameter is equal to 0, then there are no [in, out] interfaces.

### -field cOutInterfacesMax

If this parameter has a value greater or equal to 0, then the value is an absolute upper bound on the number [out] interfaces. If this parameter is less than 0, then the method may have an unbounded number of [out] interfaces. If this parameter is equal to 0, then there are no [out] interfaces.

### -field cTopLevelInInterfaces

The number of parameters that are in interface pointers.

### -field iid

The interface ID.

### -field cMethod

The number of methods in <b>iid</b>.

### -field cParams

The number of parameters in <b>imethod</b>. The receiver is excluded.

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallindirect">ICallIndirect</a>
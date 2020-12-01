---
UID: NF:rtmv2.RtmInvokeMethod
title: RtmInvokeMethod function (rtmv2.h)
description: The RtmInvokeMethod function invokes a method exported by another client.
helpviewer_keywords: ["RtmInvokeMethod","RtmInvokeMethod function [RAS]","_rtmv2ref_rtminvokemethod","rras.rtminvokemethod","rtmv2/RtmInvokeMethod"]
old-location: rras\rtminvokemethod.htm
tech.root: RRAS
ms.assetid: 97506565-2fa7-4ff7-b397-7ab712759a5d
ms.date: 12/05/2018
ms.keywords: RtmInvokeMethod, RtmInvokeMethod function [RAS], _rtmv2ref_rtminvokemethod, rras.rtminvokemethod, rtmv2/RtmInvokeMethod
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
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtmInvokeMethod
 - rtmv2/RtmInvokeMethod
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmInvokeMethod
---

# RtmInvokeMethod function


## -description

The 
<b>RtmInvokeMethod</b> function invokes a method exported by another client.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param EntityHandle [in]

Handle to the client whose methods are being invoked.

### -param Input [in]

Pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_method_input">RTM_ENTITY_METHOD_INPUT</a> structure that contains the method to be invoked and a common input buffer.

### -param OutputSize [in, out]

On input, <i>OutputSize</i> is a pointer to a <b>UINT</b> value that specifies the size, in bytes, of <i>Output</i>. 




On output, <i>OutputSize</i> receives a pointer to a <b>UINT</b> value that specifies the actual size, in bytes, of <i>Output</i>.

### -param Output [out]

Receives a pointer to an array of 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_method_output">RTM_ENTITY_METHOD_OUTPUT</a> structures. Each structure consists of a (method identifier, correct output) tuple.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

For sample code using this function, see 
<a href="/windows/desktop/RRAS/obtain-and-call-the-exported-methods-for-a-client">Obtain and Call the Exported Methods for a Client</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_method_input">RTM_ENTITY_METHOD_INPUT</a>



<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_entity_method_output">RTM_ENTITY_METHOD_OUTPUT</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmblockmethods">RtmBlockMethods</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetentitymethods">RtmGetEntityMethods</a>
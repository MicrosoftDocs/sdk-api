---
UID: NN:callobj.ICallFrame
title: ICallFrame (callobj.h)
description: Enables manipulation of call frames such as stack frames.
helpviewer_keywords: ["ICallFrame","ICallFrame interface [COM]","ICallFrame interface [COM]","described","_com_icallframe_interface","callobj/ICallFrame","com.icallframe"]
old-location: com\icallframe.htm
tech.root: com
ms.assetid: 56a75123-f402-4187-af13-d31f72a5f094
ms.date: 12/05/2018
ms.keywords: ICallFrame, ICallFrame interface [COM], ICallFrame interface [COM],described, _com_icallframe_interface, callobj/ICallFrame, com.icallframe
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
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
 - ICallFrame
 - callobj/ICallFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallFrame
---

# ICallFrame interface


## -description

Enables manipulation of call frames such as stack frames. The call frame is the body of information that a procedure must save to allow it to properly return to its caller. A call frame may exist on the stack or in registers. A stack frame maintains its caller's context information on the stack.

An instance of the <b>ICallFrame</b> interface can perform various transformations on a call frame. The call can be marshaled or persisted. The instance of this interface is bound and has an associated method number.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallFrame</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICallFrame</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICallFrame</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-copy">Copy</a>
</td>
<td align="left" width="63%">
Creates a copy of this call frame and all of its associated data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-free">Free</a>
</td>
<td align="left" width="63%">
Frees the frame copy to avoid a memory leak.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-freeparam">FreeParam</a>
</td>
<td align="left" width="63%">
Frees the specified parameter in the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-getiidandmethod">GetIIDAndMethod</a>
</td>
<td align="left" width="63%">
Retrieves the interface ID or the method number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-getmarshalsizemax">GetMarshalSizeMax</a>
</td>
<td align="left" width="63%">
Retrieves an upper bound on the number of bytes needed to marshal the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-getnames">GetNames</a>
</td>
<td align="left" width="63%">
Retrieves the method or interface name of this call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-getparam">GetParam</a>
</td>
<td align="left" width="63%">
Retrieves the value of a specified parameter in the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-getparaminfo">GetParamInfo</a>
</td>
<td align="left" width="63%">
Retrieves the information for the specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-getreturnvalue">GetReturnValue</a>
</td>
<td align="left" width="63%">
Retrieves the return value stored in the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-getstacklocation">GetStackLocation</a>
</td>
<td align="left" width="63%">
Retrieves the stack location onto which this call frame is bound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Applies this activation record to an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-marshal">Marshal</a>
</td>
<td align="left" width="63%">
Marshals the call frame by turning its reachable data into a flat buffer without disturbing the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-releasemarshaldata">ReleaseMarshalData</a>
</td>
<td align="left" width="63%">
Releases resources that are held by interface pointers residing in a packet of marshaled data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-setparam">SetParam</a>
</td>
<td align="left" width="63%">
Sets the value of a specified parameter in the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-setreturnvalue">SetReturnValue</a>
</td>
<td align="left" width="63%">
Sets the return value within the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-setstacklocation">SetStackLocation</a>
</td>
<td align="left" width="63%">
Sets the stack location onto which this call frame is bound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-unmarshal">Unmarshal</a>
</td>
<td align="left" width="63%">
Unmarshals a packet of data containing the previously marshaled [out] parameters of a call into this already existing activation record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nf-callobj-icallframe-walkframe">WalkFrame</a>
</td>
<td align="left" width="63%">
Searches for interface pointers that are reachable from [in], [in, out], or [out] parameters of the frame.

</td>
</tr>
</table>


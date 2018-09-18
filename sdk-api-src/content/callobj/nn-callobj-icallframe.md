---
UID: NN:callobj.ICallFrame
title: ICallFrame
author: windows-sdk-content
description: Enables manipulation of call frames such as stack frames.
old-location: com\icallframe.htm
tech.root: com
ms.assetid: 56a75123-f402-4187-af13-d31f72a5f094
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: ICallFrame, ICallFrame interface [COM], ICallFrame interface [COM],described, _com_icallframe_interface, callobj/ICallFrame, com.icallframe
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICallFrame interface


## -description


Enables manipulation of call frames such as stack frames. The call frame is the body of information that a procedure must save to allow it to properly return to its caller. A call frame may exist on the stack or in registers. A stack frame maintains its caller's context information on the stack.

An instance of the <b>ICallFrame</b> interface can perform various transformations on a call frame. The call can be marshaled or persisted. The instance of this interface is bound and has an associated method number.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallFrame</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ICallFrame</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/bf2d2e55-d9d1-48d6-817c-382c739d1acd">Copy</a>
</td>
<td align="left" width="63%">
Creates a copy of this call frame and all of its associated data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97261d93-40cf-4a27-9bee-677600c04699">Free</a>
</td>
<td align="left" width="63%">
Frees the frame copy to avoid a memory leak.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b141bfc4-de1b-4251-b88f-551d0805e9b6">FreeParam</a>
</td>
<td align="left" width="63%">
Frees the specified parameter in the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/938798ef-ddc8-4182-9216-d130c4f0e4ae">GetIIDAndMethod</a>
</td>
<td align="left" width="63%">
Retrieves the interface ID or the method number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/807b4542-c18d-48e4-8493-c40a85e5e1de">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e564b29-8b21-4e65-981e-4ceda1d7774d">GetMarshalSizeMax</a>
</td>
<td align="left" width="63%">
Retrieves an upper bound on the number of bytes needed to marshal the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3efb0819-51db-419b-a9f1-710bb3abae2d">GetNames</a>
</td>
<td align="left" width="63%">
Retrieves the method or interface name of this call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43662600-841c-4237-80ac-3822eb47be88">GetParam</a>
</td>
<td align="left" width="63%">
Retrieves the value of a specified parameter in the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb75930d-8e1b-4e97-87f2-bb9d171658a8">GetParamInfo</a>
</td>
<td align="left" width="63%">
Retrieves the information for the specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb03e968-37af-46fd-b2ed-08c5ef8eb265">GetReturnValue</a>
</td>
<td align="left" width="63%">
Retrieves the return value stored in the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e6b5e52-78bb-47cd-9019-efb5c0860a6d">GetStackLocation</a>
</td>
<td align="left" width="63%">
Retrieves the stack location onto which this call frame is bound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75cb7b96-55c9-4aee-b507-a549e2af38bc">Invoke</a>
</td>
<td align="left" width="63%">
Applies this activation record to an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cab40c31-1f89-4da9-a1e0-ef946b34665c">Marshal</a>
</td>
<td align="left" width="63%">
Marshals the call frame by turning its reachable data into a flat buffer without disturbing the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c82107ad-68d1-4a46-ba78-37592d445c57">ReleaseMarshalData</a>
</td>
<td align="left" width="63%">
Releases resources that are held by interface pointers residing in a packet of marshaled data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec828206-d49f-49da-91fc-554d703b53db">SetParam</a>
</td>
<td align="left" width="63%">
Sets the value of a specified parameter in the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/848cccc7-19c8-4ce6-b609-bcf798ec8c76">SetReturnValue</a>
</td>
<td align="left" width="63%">
Sets the return value within the call frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/689f3819-488b-4679-a401-f1500db22461">SetStackLocation</a>
</td>
<td align="left" width="63%">
Sets the stack location onto which this call frame is bound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f604366-0e1f-4e04-9843-13c77ea573ab">Unmarshal</a>
</td>
<td align="left" width="63%">
Unmarshals a packet of data containing the previously marshaled [out] parameters of a call into this already existing activation record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64e4967b-6b54-4416-ae10-04987f13d39a">WalkFrame</a>
</td>
<td align="left" width="63%">
Searches for interface pointers that are reachable from [in], [in, out], or [out] parameters of the frame.

</td>
</tr>
</table> 


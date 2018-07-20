---
UID: NN:objidl.IBindCtx
title: IBindCtx
author: windows-sdk-content
description: Provides access to a bind context, which is an object that stores information about a particular moniker binding operation.
old-location: com\ibindctx.htm
old-project: com
ms.assetid: e4c8abb5-0c89-44dd-8d95-efbfcc999b46
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IBindCtx, IBindCtx interface [COM], IBindCtx interface [COM],described, _com_ibindctx, com.ibindctx, objidl/IBindCtx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IBindCtx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IBindCtx interface


## -description


Provides access to a bind context, which is an object that stores information about a particular moniker binding operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBindCtx</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IBindCtx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBindCtx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e799ce4-e9b3-4b31-98a0-2167a0c19848">EnumObjectParam</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an interface that can be used to enumerate the keys of the bind context's string-keyed table of pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccb239ee-922f-4e66-8aca-7651c0243a2b">GetBindOptions</a>
</td>
<td align="left" width="63%">
Retrieves the binding options stored in this bind context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f423495-7a34-4901-968e-1fe204680d8a">GetObjectParam</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer to the object associated with the specified key in the bind context's string-keyed table of pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26938d07-d772-4e72-a6aa-57dd2f2cece1">GetRunningObjectTable</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer to the running object table (ROT) for the computer on which this bind context is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84d49231-5fdd-4a89-8e76-1f0e56bc553f">RegisterObjectBound</a>
</td>
<td align="left" width="63%">
Registers an object with the bind context to ensure that the object remains active until the bind context is released.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ee2b5b2-9b9c-41f1-8e58-7432ebc0f9ed">RegisterObjectParam</a>
</td>
<td align="left" width="63%">
Associates an object with a string key in the bind context's string-keyed table of pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12107633-6e7f-4d41-8e5c-5739cff98552">ReleaseBoundObjects</a>
</td>
<td align="left" width="63%">
Releases all pointers to all objects that were previously registered by calls to <a href="https://msdn.microsoft.com/84d49231-5fdd-4a89-8e76-1f0e56bc553f">RegisterObjectBound</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c49421a3-1733-4f54-8e30-d23641f13c38">RevokeObjectBound</a>
</td>
<td align="left" width="63%">
Removes the object from the bind context, undoing a previous call to <a href="https://msdn.microsoft.com/84d49231-5fdd-4a89-8e76-1f0e56bc553f">RegisterObjectBound</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7dbf9c8-0ecf-4076-8bec-4da457c60cee">RevokeObjectParam</a>
</td>
<td align="left" width="63%">
Removes the specified key and its associated pointer from the bind context's string-keyed table of objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dcce48e-567e-42b4-8df2-2bc861cb5fcb">SetBindOptions</a>
</td>
<td align="left" width="63%">
Sets new values for the binding parameters stored in the bind context.

</td>
</tr>
</table> 


## -remarks



A bind context includes the following information:

<ul>
<li>A <a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a> structure containing a set of parameters that do not change during the binding operation. When a composite moniker is bound, each component uses the same bind context, so it acts as a mechanism for passing the same parameters to each component of a composite moniker. 
</li>
<li>A set of pointers to objects that the binding operation has activated. The bind context holds pointers to these bound objects, keeping them loaded and thus eliminating redundant activations if the objects are needed again during subsequent binding operations.</li>
<li>A pointer to the running object table (ROT) on the same computer as the process that started the bind operation. Moniker implementations that need to access the ROT should use the <a href="https://msdn.microsoft.com/26938d07-d772-4e72-a6aa-57dd2f2cece1">IBindCtx::GetRunningObjectTable</a> method rather than using the <a href="https://msdn.microsoft.com/65d9cf7d-cc8a-4199-9a4a-7fd67ef8872d">GetRunningObjectTable</a> function. This allows future enhancements to the system's <b>IBindCtx</b> implementation to modify binding behavior.
</li>
<li>A table of interface pointers, each associated with a string key. This capability enables moniker implementations to store interface pointers under a well-known string so that they can later be retrieved from the bind context. For example, OLE defines several string keys ("ExceededDeadline", "ConnectManually", and so on) that can be used to store a pointer to the object that caused an error during a binding operation.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a>



<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>



<a href="https://msdn.microsoft.com/fe306a36-da24-4b1e-ab42-359d37962d36">IOleItemContainer</a>



<a href="https://msdn.microsoft.com/37844d9b-35ce-4d30-8a58-dac4c671896f">IParseDisplayName</a>
 

 


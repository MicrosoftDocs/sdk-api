---
UID: NN:objidl.IBindCtx
title: IBindCtx (objidl.h)
author: windows-sdk-content
description: Provides access to a bind context, which is an object that stores information about a particular moniker binding operation.
old-location: com\ibindctx.htm
tech.root: com
ms.assetid: e4c8abb5-0c89-44dd-8d95-efbfcc999b46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBindCtx, IBindCtx interface [COM], IBindCtx interface [COM],described, _com_ibindctx, com.ibindctx, objidl/IBindCtx
ms.topic: interface
f1_keywords: 
 - "objidl/IBindCtx"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IBindCtx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBindCtx interface


## -description


Provides access to a bind context, which is an object that stores information about a particular moniker binding operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBindCtx</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBindCtx</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-enumobjectparam">EnumObjectParam</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an interface that can be used to enumerate the keys of the bind context's string-keyed table of pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-getbindoptions">GetBindOptions</a>
</td>
<td align="left" width="63%">
Retrieves the binding options stored in this bind context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam">GetObjectParam</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer to the object associated with the specified key in the bind context's string-keyed table of pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-getrunningobjecttable">GetRunningObjectTable</a>
</td>
<td align="left" width="63%">
Retrieves an interface pointer to the running object table (ROT) for the computer on which this bind context is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectbound">RegisterObjectBound</a>
</td>
<td align="left" width="63%">
Registers an object with the bind context to ensure that the object remains active until the bind context is released.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">RegisterObjectParam</a>
</td>
<td align="left" width="63%">
Associates an object with a string key in the bind context's string-keyed table of pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-releaseboundobjects">ReleaseBoundObjects</a>
</td>
<td align="left" width="63%">
Releases all pointers to all objects that were previously registered by calls to <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectbound">RegisterObjectBound</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-revokeobjectbound">RevokeObjectBound</a>
</td>
<td align="left" width="63%">
Removes the object from the bind context, undoing a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectbound">RegisterObjectBound</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-revokeobjectparam">RevokeObjectParam</a>
</td>
<td align="left" width="63%">
Removes the specified key and its associated pointer from the bind context's string-keyed table of objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-setbindoptions">SetBindOptions</a>
</td>
<td align="left" width="63%">
Sets new values for the binding parameters stored in the bind context.

</td>
</tr>
</table> 


## -remarks



A bind context includes the following information:

<ul>
<li>A <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure containing a set of parameters that do not change during the binding operation. When a composite moniker is bound, each component uses the same bind context, so it acts as a mechanism for passing the same parameters to each component of a composite moniker. 
</li>
<li>A set of pointers to objects that the binding operation has activated. The bind context holds pointers to these bound objects, keeping them loaded and thus eliminating redundant activations if the objects are needed again during subsequent binding operations.</li>
<li>A pointer to the running object table (ROT) on the same computer as the process that started the bind operation. Moniker implementations that need to access the ROT should use the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-getrunningobjecttable">IBindCtx::GetRunningObjectTable</a> method rather than using the <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-getrunningobjecttable">GetRunningObjectTable</a> function. This allows future enhancements to the system's <b>IBindCtx</b> implementation to modify binding behavior.
</li>
<li>A table of interface pointers, each associated with a string key. This capability enables moniker implementations to store interface pointers under a well-known string so that they can later be retrieved from the bind context. For example, OLE defines several string keys ("ExceededDeadline", "ConnectManually", and so on) that can be used to store a pointer to the object that caused an error during a binding operation.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a>
 

 


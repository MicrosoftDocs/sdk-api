---
UID: NF:objidl.IBindCtx.RevokeObjectBound
title: IBindCtx::RevokeObjectBound (objidl.h)
author: windows-sdk-content
description: Removes the object from the bind context, undoing a previous call to RegisterObjectBound.
old-location: com\ibindctx_revokeobjectbound.htm
tech.root: com
ms.assetid: c49421a3-1733-4f54-8e30-d23641f13c38
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBindCtx interface [COM],RevokeObjectBound method, IBindCtx.RevokeObjectBound, IBindCtx::RevokeObjectBound, RevokeObjectBound, RevokeObjectBound method [COM], RevokeObjectBound method [COM],IBindCtx interface, _com_ibindctx_revokeobjectbound, com.ibindctx_revokeobjectbound, objidl/IBindCtx::RevokeObjectBound
ms.topic: method
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
 - IBindCtx.RevokeObjectBound
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBindCtx::RevokeObjectBound


## -description


Removes the object from the bind context, undoing a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectbound">RegisterObjectBound</a>.


## -parameters




### -param punk [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/com/iunknown-and-interface-inheritance">IUnknown</a> interface on the object to be removed.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The object was released successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOTBOUND</b></dt>
</dl>
</td>
<td width="60%">
The object was not previously registered.

</td>
</tr>
</table>
 




## -remarks



You would rarely call this method. It is documented primarily for completeness.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>
 

 


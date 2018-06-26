---
UID: NF:objidl.IBindCtx.RevokeObjectParam
title: IBindCtx::RevokeObjectParam
author: windows-sdk-content
description: Removes the specified key and its associated pointer from the bind context's string-keyed table of objects. The key must have previously been inserted into the table with a call to RegisterObjectParam.
old-location: com\ibindctx_revokeobjectparam.htm
old-project: com
ms.assetid: e7dbf9c8-0ecf-4076-8bec-4da457c60cee
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IBindCtx interface [COM],RevokeObjectParam method, IBindCtx.RevokeObjectParam, IBindCtx::RevokeObjectParam, RevokeObjectParam, RevokeObjectParam method [COM], RevokeObjectParam method [COM],IBindCtx interface, _com_ibindctx_revokeobjectparam, com.ibindctx_revokeobjectparam, objidl/IBindCtx::RevokeObjectParam
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
 - IBindCtx.RevokeObjectParam
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IBindCtx::RevokeObjectParam


## -description


Removes the specified key and its associated pointer from the bind context's string-keyed table of objects. The key must have previously been inserted into the table with a call to <a href="https://msdn.microsoft.com/7ee2b5b2-9b9c-41f1-8e58-7432ebc0f9ed">RegisterObjectParam</a>.


## -parameters




### -param pszKey [in]

The <a href="_shell_STR_constants_cpp">bind context string key</a> to be removed. Key string comparison is case-sensitive.


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
The specified key was removed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object was not previously registered.

</td>
</tr>
</table>
 




## -remarks



A bind context maintains a table of interface pointers, each associated with a string key. This enables communication between a moniker implementation and the caller that initiated the binding operation. One party can store an interface pointer under a string known to both parties so that the other party can later retrieve it from the bind context.

This method is used to remove an entry from the table. If the specified key is found, the bind context also releases its reference to the object.




## -see-also




<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>
 

 


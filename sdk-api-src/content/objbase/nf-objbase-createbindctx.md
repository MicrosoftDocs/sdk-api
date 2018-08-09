---
UID: NF:objbase.CreateBindCtx
title: CreateBindCtx function
author: windows-sdk-content
description: Returns a pointer to an implementation of IBindCtx (a bind context object). This object stores information about a particular moniker-binding operation.
old-location: com\createbindctx.htm
old-project: com
ms.assetid: 0f0ded09-7a7c-40bb-8198-b9f5058827d4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateBindCtx, CreateBindCtx function [COM], _com_CreateBindCtx, com.createbindctx, objbase/CreateBindCtx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: COMSD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-OLE32-IE-l1-1-0.dll
 - ole32_wp.dll
 - Ext-MS-Win-OLE32-bindctx-l1-1-0.dll
api_name:
 - CreateBindCtx
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# CreateBindCtx function


## -description


Returns a pointer to an implementation of <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> (a bind context object). This object stores information about a particular moniker-binding operation.


## -parameters




### -param reserved [in]

This parameter is reserved and must be 0.


### -param ppbc [out]

Address of an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>* pointer variable that receives the interface pointer to the new bind context object. When the function is successful, the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the bind context. A <b>NULL</b> value for the bind context indicates that an error occurred.


## -returns



This function can return the standard return values E_OUTOFMEMORY and S_OK.




## -remarks



<b>CreateBindCtx</b> is most commonly used in the process of binding a moniker (locating and getting a pointer to an interface by identifying it through a moniker), as in the following steps:

<ol>
<li>Get a pointer to a bind context by calling the <b>CreateBindCtx</b> function.
</li>
<li>Call the <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> method on the moniker, retrieving an interface pointer to the object to which the moniker refers. 
</li>
<li>Release the bind context.</li>
<li>Use the interface pointer.</li>
<li>Release the interface pointer.</li>
</ol>
The following code fragment illustrates these steps.

<pre class="syntax" xml:space="preserve"><code>// pMnk is an IMoniker * that points to a previously acquired moniker 
IInterface *pInterface; 
IBindCtx *pbc; 
 
CreateBindCtx( 0, &amp;pbc ); 
pMnk-&gt;BindToObject( pbc, NULL, IID_IInterface, &amp;pInterface ); 
pbc-&gt;Release(); 

// pInterface now points to the object; safe to use pInterface 
pInterface-&gt;Release(); 
</code></pre>
Bind contexts are also used in other methods of the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface besides <a href="https://msdn.microsoft.com/b5ce39ff-3387-4f72-9aea-5a26eed3810c">IMoniker::BindToObject</a> and in the <a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a> function. 

A bind context retains references to the objects that are bound during the binding operation, causing the bound objects to remain active (keeping the object's server running) until the bind context is released. Reusing a bind context when subsequent operations bind to the same object can improve performance. You should, however, release the bind context as soon as possible, because you could be keeping the objects activated unnecessarily.

A bind context contains a <a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a> structure, which contains parameters that apply to all steps in a binding operation. When you create a bind context using <b>CreateBindCtx</b>, the fields of the <b>BIND_OPTS</b> structure are initialized as follows.

<pre class="syntax" xml:space="preserve"><code>cbStruct = sizeof(BIND_OPTS) 
grfFlags = 0 
grfMode = STGM_READWRITE 
dwTickCountDeadline = 0</code></pre>
You can call the <a href="https://msdn.microsoft.com/9dcce48e-567e-42b4-8df2-2bc861cb5fcb">IBindCtx::SetBindOptions</a> method to modify these default values.




## -see-also




<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>



<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>



<a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a>
 

 


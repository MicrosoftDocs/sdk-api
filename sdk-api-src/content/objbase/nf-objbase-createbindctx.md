---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


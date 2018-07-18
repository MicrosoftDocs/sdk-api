---
UID: NF:objidl.IBindCtx.SetBindOptions
title: IBindCtx::SetBindOptions
author: windows-sdk-content
description: Sets new values for the binding parameters stored in the bind context.
old-location: com\ibindctx_setbindoptions.htm
old-project: com
ms.assetid: 9dcce48e-567e-42b4-8df2-2bc861cb5fcb
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IBindCtx interface [COM],SetBindOptions method, IBindCtx.SetBindOptions, IBindCtx::SetBindOptions, SetBindOptions, SetBindOptions method [COM], SetBindOptions method [COM],IBindCtx interface, _com_ibindctx_setbindoptions, com.ibindctx_setbindoptions, objidl/IBindCtx::SetBindOptions
ms.prod: windows
ms.technology: windows-sdk
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
 - IBindCtx.SetBindOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IBindCtx::SetBindOptions


## -description


Sets new values for the binding parameters stored in the bind context.


## -parameters




### -param pbindopts [in]

A pointer to a <a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a>, <a href="https://msdn.microsoft.com/fb2aa8c1-dddc-480e-b544-61a1074125ef">BIND_OPTS2</a>, or <a href="https://msdn.microsoft.com/7e668313-229a-4d04-b8a2-d5072c87a5b5">BIND_OPTS3</a> structure containing the binding parameters.


## -returns



This method can return the standard return values E_OUTOFMEMORY and S_OK.




## -remarks



A bind context contains a block of parameters that are common to most <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> operations. These parameters do not change as the operation moves from piece to piece of a composite moniker.

Subsequent binding operations can call <a href="https://msdn.microsoft.com/ccb239ee-922f-4e66-8aca-7651c0243a2b">IBindCtx::GetBindOptions</a> to retrieve these parameters.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
This method can be called by moniker clients (those who use monikers to acquire interface pointers to objects).

When you first create a bind context by using the <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> function, the fields of the <a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a> structure are initialized to the following values:

<pre class="syntax" xml:space="preserve"><code>    cbStruct = sizeof(BIND_OPTS); 
    grfFlags = 0; 
    grfMode = STGM_READWRITE; 
    dwTickCountDeadline = 0; 
</code></pre>
You can use the <b>IBindCtx::SetBindOptions</b> method to modify these values before using the bind context, if you want values other than the defaults.

<b>SetBindOptions</b> copies the members of the specified structure, but not the <a href="https://msdn.microsoft.com/88c94a7f-5cf0-4d61-833f-91cba45d8624">COSERVERINFO</a> structure and the pointers it contains. Callers may not free these pointers until the bind context is released.




## -see-also




<a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a>



<a href="https://msdn.microsoft.com/fb2aa8c1-dddc-480e-b544-61a1074125ef">BIND_OPTS2</a>



<a href="https://msdn.microsoft.com/7e668313-229a-4d04-b8a2-d5072c87a5b5">BIND_OPTS3</a>



<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>
 

 


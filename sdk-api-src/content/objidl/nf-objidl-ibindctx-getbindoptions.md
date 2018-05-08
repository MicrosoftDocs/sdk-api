---
UID: NF:objidl.IBindCtx.GetBindOptions
title: IBindCtx::GetBindOptions
author: windows-driver-content
description: Retrieves the binding options stored in this bind context.
old-location: com\ibindctx_getbindoptions.htm
old-project: com
ms.assetid: ccb239ee-922f-4e66-8aca-7651c0243a2b
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: GetBindOptions, GetBindOptions method [COM], GetBindOptions method [COM],IBindCtx interface, IBindCtx interface [COM],GetBindOptions method, IBindCtx.GetBindOptions, IBindCtx::GetBindOptions, _com_ibindctx_getbindoptions, com.ibindctx_getbindoptions, objidl/IBindCtx::GetBindOptions
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IBindCtx.GetBindOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IBindCtx::GetBindOptions


## -description


Retrieves the binding options stored in this bind context.


## -parameters




### -param pbindopts [in, out]

A pointer to an initialized structure that receives the current binding parameters on return. See <a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a>, <a href="https://msdn.microsoft.com/fb2aa8c1-dddc-480e-b544-61a1074125ef">BIND_OPTS2</a>, and <a href="https://msdn.microsoft.com/7e668313-229a-4d04-b8a2-d5072c87a5b5">BIND_OPTS3</a>.


## -returns



This method can return the standard return values E_UNEXPECTED and S_OK.




## -remarks



A bind context contains a block of parameters that are common to most <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> operations and that do not change as the operation moves from piece to piece of a composite moniker.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You typically call this method if you are writing your own moniker class. (This requires that you implement the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface.) You call this method to retrieve the parameters specified by the moniker client.

You must initialize the structure that is filled in by this method. Before calling this method, you must initialize the <b>cbStruct</b> member to the size of the structure.




## -see-also




<a href="https://msdn.microsoft.com/764f09c9-ff20-4ae2-b94f-4b0a1e117e49">BIND_OPTS</a>



<a href="https://msdn.microsoft.com/fb2aa8c1-dddc-480e-b544-61a1074125ef">BIND_OPTS2</a>



<a href="https://msdn.microsoft.com/7e668313-229a-4d04-b8a2-d5072c87a5b5">BIND_OPTS3</a>



<a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>
 

 


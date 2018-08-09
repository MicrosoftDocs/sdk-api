---
UID: NF:tapi3if.ITPhone.get_Terminals
title: ITPhone::get_Terminals
author: windows-sdk-content
description: The get_Terminals method retrieves a collection of terminals that are associated with the phone. The application does not have to call ITPhone::Open before executing this method.
old-location: tapi3\itphone_get_terminals.htm
old-project: tapi
ms.assetid: 09e5921c-c7da-40fc-902a-1e22ebe19b0a
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_Terminals method, ITPhone.get_Terminals, ITPhone::get_Terminals, _tapi3_itphone_get_terminals, get_Terminals, get_Terminals method [TAPI 2.2], get_Terminals method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_terminals, tapi3if/ITPhone::get_Terminals
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhone.get_Terminals
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhone::get_Terminals


## -description


The 
<b>get_Terminals</b> method retrieves a collection of terminals that are associated with the phone. The application does not have to call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before executing this method.


## -parameters




### -param pAddress [in]

Pointer to the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface.


### -param pTerminals [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface pointers.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If no terminals are associated with the phone, this method produces an empty collection and returns S_OK.

The application does not have to call the 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> method before calling 
<b>get_Terminals</b>. This is because the implementation of the phone object can open the phone and call 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>interface returned by <b>ITPhone::get_Terminals</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b>interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 


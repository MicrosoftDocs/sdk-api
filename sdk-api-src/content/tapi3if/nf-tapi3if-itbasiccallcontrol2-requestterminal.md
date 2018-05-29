---
UID: NF:tapi3if.ITBasicCallControl2.RequestTerminal
title: ITBasicCallControl2::RequestTerminal
author: windows-sdk-content
description: The RequestTerminal method gets a suitable terminal, given the class, media, and direction required.
old-location: tapi3\itbasiccallcontrol2_requestterminal.htm
old-project: Tapi
ms.assetid: 20b7266c-8990-457c-94cf-18cc2bed6b21
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITBasicCallControl2 interface [TAPI 2.2],RequestTerminal method, ITBasicCallControl2.RequestTerminal, ITBasicCallControl2::RequestTerminal, RequestTerminal, RequestTerminal method [TAPI 2.2], RequestTerminal method [TAPI 2.2],ITBasicCallControl2 interface, _tapi3_itbasiccallcontrol2_requestterminal, tapi3.itbasiccallcontrol2_requestterminal, tapi3if/ITBasicCallControl2::RequestTerminal
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITBasicCallControl2.RequestTerminal
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITBasicCallControl2::RequestTerminal


## -description


The 
<b>RequestTerminal</b> method gets a suitable terminal, given the class, media, and direction required.


## -parameters




### -param bstrTerminalClassGUID [in]

The terminal class required for the call.


### -param lMediaType [in]

Bitwise ORed list of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a> required for the call.


### -param Direction [in]

The 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a> descriptor for the terminal.


### -param ppTerminal [out]

Pointer to 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>AddRef</b> method is automatically called on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface returned by this method. The application must call the <b>Release</b> method on the 
<b>ITTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/fc693221-b7ba-4b33-aed7-59ec92fc9b58">ITBasicCallControl2</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 


---
UID: NF:tapi3if.ITPhone.EnumerateTerminals
title: ITPhone::EnumerateTerminals
author: windows-sdk-content
description: The EnumerateTerminals method retrieves an enumeration of terminals that are associated with the phone. The application does not have to call ITPhone::Open before executing this method.
old-location: tapi3\itphone_enumerateterminals.htm
old-project: Tapi
ms.assetid: 87c756e3-abd0-4dff-b815-ff7dd60902f7
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: EnumerateTerminals, EnumerateTerminals method [TAPI 2.2], EnumerateTerminals method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],EnumerateTerminals method, ITPhone.EnumerateTerminals, ITPhone::EnumerateTerminals, _tapi3_itphone_enumerateterminals, tapi3.itphone_enumerateterminals, tapi3if/ITPhone::EnumerateTerminals
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITPhone.EnumerateTerminals
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhone::EnumerateTerminals


## -description


The 
<b>EnumerateTerminals</b> method retrieves an enumeration of terminals that are associated with the phone. The application does not have to call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before executing this method.


## -parameters




### -param pAddress [in]

Pointer to 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface.


### -param ppEnumTerminal [out]

Pointer to the 
<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a> interface that enumerates terminals.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If no terminals are associated with the phone, this method produces an empty enumeration and returns S_OK.

Although the 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> function requires the handle to an open phone device, the application does not have to call the 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> method before calling 
<b>EnumerateTerminals</b>. This is because the implementation of the phone object can open the phone and call 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a> interface returned by <b>ITPhone::EnumerateTerminals</b>. The application must call <b>Release</b> on the 
<b>IEnumTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>
 

 


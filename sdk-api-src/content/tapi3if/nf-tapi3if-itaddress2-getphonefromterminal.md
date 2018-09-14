---
UID: NF:tapi3if.ITAddress2.GetPhoneFromTerminal
title: ITAddress2::GetPhoneFromTerminal
author: windows-sdk-content
description: The GetPhoneFromTerminal method returns the phone object associated with the terminal. Only one phone can be associated with a terminal.
old-location: tapi3\itaddress2_getphonefromterminal.htm
tech.root: TAPI
ms.assetid: 0d3873ad-ce3d-4b4c-907f-9c0dbf0ef206
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetPhoneFromTerminal, GetPhoneFromTerminal method [TAPI 2.2], GetPhoneFromTerminal method [TAPI 2.2],ITAddress2 interface, ITAddress2 interface [TAPI 2.2],GetPhoneFromTerminal method, ITAddress2.GetPhoneFromTerminal, ITAddress2::GetPhoneFromTerminal, _tapi3_itaddress2_getphonefromterminal, tapi3.itaddress2_getphonefromterminal, tapi3if/ITAddress2::GetPhoneFromTerminal
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddress2.GetPhoneFromTerminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress2::GetPhoneFromTerminal


## -description


The 
<b>GetPhoneFromTerminal</b> method returns the phone object associated with the terminal. Only one phone can be associated with a terminal.


## -parameters




### -param pTerminal [in]

Pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


### -param ppPhone [out]

Pointer to the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3cc47291-8130-45bd-8db8-c5d1b463507d">ITAddress2</a>



<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 


---
UID: NF:tapi3if.ITBasicCallControl2.UnselectTerminalOnCall
title: ITBasicCallControl2::UnselectTerminalOnCall
author: windows-sdk-content
description: The UnselectTerminalOnCall method unselects a terminal from the call.
old-location: tapi3\itbasiccallcontrol2_unselectterminaloncall.htm
tech.root: tapi
ms.assetid: 93795757-58b6-4eb5-9d0c-f7c0a3bb9695
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITBasicCallControl2 interface [TAPI 2.2],UnselectTerminalOnCall method, ITBasicCallControl2.UnselectTerminalOnCall, ITBasicCallControl2::UnselectTerminalOnCall, UnselectTerminalOnCall, UnselectTerminalOnCall method [TAPI 2.2], UnselectTerminalOnCall method [TAPI 2.2],ITBasicCallControl2 interface, _tapi3_itbasiccallcontrol2_unselectterminaloncall, tapi3.itbasiccallcontrol2_unselectterminaloncall, tapi3if/ITBasicCallControl2::UnselectTerminalOnCall
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
 - ITBasicCallControl2.UnselectTerminalOnCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITBasicCallControl2::UnselectTerminalOnCall


## -description


The 
<b>UnselectTerminalOnCall</b> method unselects a terminal from the call.


## -parameters




### -param pTerminal [in]

Pointer to 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fc693221-b7ba-4b33-aed7-59ec92fc9b58">ITBasicCallControl2</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 


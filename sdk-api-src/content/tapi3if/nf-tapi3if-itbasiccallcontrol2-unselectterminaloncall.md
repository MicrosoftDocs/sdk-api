---
UID: NF:tapi3if.ITBasicCallControl2.UnselectTerminalOnCall
title: ITBasicCallControl2::UnselectTerminalOnCall (tapi3if.h)
description: The UnselectTerminalOnCall method unselects a terminal from the call.
helpviewer_keywords: ["ITBasicCallControl2 interface [TAPI 2.2]","UnselectTerminalOnCall method","ITBasicCallControl2.UnselectTerminalOnCall","ITBasicCallControl2::UnselectTerminalOnCall","UnselectTerminalOnCall","UnselectTerminalOnCall method [TAPI 2.2]","UnselectTerminalOnCall method [TAPI 2.2]","ITBasicCallControl2 interface","_tapi3_itbasiccallcontrol2_unselectterminaloncall","tapi3.itbasiccallcontrol2_unselectterminaloncall","tapi3if/ITBasicCallControl2::UnselectTerminalOnCall"]
old-location: tapi3\itbasiccallcontrol2_unselectterminaloncall.htm
tech.root: tapi3
ms.assetid: 93795757-58b6-4eb5-9d0c-f7c0a3bb9695
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl2 interface [TAPI 2.2],UnselectTerminalOnCall method, ITBasicCallControl2.UnselectTerminalOnCall, ITBasicCallControl2::UnselectTerminalOnCall, UnselectTerminalOnCall, UnselectTerminalOnCall method [TAPI 2.2], UnselectTerminalOnCall method [TAPI 2.2],ITBasicCallControl2 interface, _tapi3_itbasiccallcontrol2_unselectterminaloncall, tapi3.itbasiccallcontrol2_unselectterminaloncall, tapi3if/ITBasicCallControl2::UnselectTerminalOnCall
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITBasicCallControl2::UnselectTerminalOnCall
 - tapi3if/ITBasicCallControl2::UnselectTerminalOnCall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl2.UnselectTerminalOnCall
---

# ITBasicCallControl2::UnselectTerminalOnCall


## -description

The 
<b>UnselectTerminalOnCall</b> method unselects a terminal from the call.

## -parameters

### -param pTerminal [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2">ITBasicCallControl2</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>
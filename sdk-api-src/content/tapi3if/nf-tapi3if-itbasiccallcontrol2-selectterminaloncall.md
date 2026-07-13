---
UID: NF:tapi3if.ITBasicCallControl2.SelectTerminalOnCall
title: ITBasicCallControl2::SelectTerminalOnCall (tapi3if.h)
description: The SelectTerminalOnCall method selects the terminal onto the call.
helpviewer_keywords: ["ITBasicCallControl2 interface [TAPI 2.2]","SelectTerminalOnCall method","ITBasicCallControl2.SelectTerminalOnCall","ITBasicCallControl2::SelectTerminalOnCall","SelectTerminalOnCall","SelectTerminalOnCall method [TAPI 2.2]","SelectTerminalOnCall method [TAPI 2.2]","ITBasicCallControl2 interface","_tapi3_itbasiccallcontrol2_selectterminaloncall","tapi3.itbasiccallcontrol2_selectterminaloncall","tapi3if/ITBasicCallControl2::SelectTerminalOnCall"]
old-location: tapi3\itbasiccallcontrol2_selectterminaloncall.htm
tech.root: tapi3
ms.assetid: 87117ec1-0d61-4edb-8ed6-0d029a77e1a5
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl2 interface [TAPI 2.2],SelectTerminalOnCall method, ITBasicCallControl2.SelectTerminalOnCall, ITBasicCallControl2::SelectTerminalOnCall, SelectTerminalOnCall, SelectTerminalOnCall method [TAPI 2.2], SelectTerminalOnCall method [TAPI 2.2],ITBasicCallControl2 interface, _tapi3_itbasiccallcontrol2_selectterminaloncall, tapi3.itbasiccallcontrol2_selectterminaloncall, tapi3if/ITBasicCallControl2::SelectTerminalOnCall
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
 - ITBasicCallControl2::SelectTerminalOnCall
 - tapi3if/ITBasicCallControl2::SelectTerminalOnCall
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
 - ITBasicCallControl2.SelectTerminalOnCall
---

# ITBasicCallControl2::SelectTerminalOnCall


## -description

The 
<b>SelectTerminalOnCall</b> method selects the terminal onto the call.

## -parameters

### -param pTerminal [in]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2">ITBasicCallControl2</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>
---
UID: NF:tapi3if.ITBasicAudioTerminal.put_Balance
title: ITBasicAudioTerminal::put_Balance (tapi3if.h)
description: The put_Balance method sets the balance. This method is not implemented for terminals shipped with TAPI 3.0 and higher.
helpviewer_keywords: ["ITBasicAudioTerminal interface [TAPI 2.2]","put_Balance method","ITBasicAudioTerminal.put_Balance","ITBasicAudioTerminal::put_Balance","_tapi3_itbasicaudioterminal_put_balance","put_Balance","put_Balance method [TAPI 2.2]","put_Balance method [TAPI 2.2]","ITBasicAudioTerminal interface","tapi3.itbasicaudioterminal_put_balance","tapi3if/ITBasicAudioTerminal::put_Balance"]
old-location: tapi3\itbasicaudioterminal_put_balance.htm
tech.root: tapi3
ms.assetid: 8337376e-5de6-4d6d-9f95-49b83d438168
ms.date: 12/05/2018
ms.keywords: ITBasicAudioTerminal interface [TAPI 2.2],put_Balance method, ITBasicAudioTerminal.put_Balance, ITBasicAudioTerminal::put_Balance, _tapi3_itbasicaudioterminal_put_balance, put_Balance, put_Balance method [TAPI 2.2], put_Balance method [TAPI 2.2],ITBasicAudioTerminal interface, tapi3.itbasicaudioterminal_put_balance, tapi3if/ITBasicAudioTerminal::put_Balance
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
 - ITBasicAudioTerminal::put_Balance
 - tapi3if/ITBasicAudioTerminal::put_Balance
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
 - ITBasicAudioTerminal.put_Balance
---

# ITBasicAudioTerminal::put_Balance


## -description

The 
<b>put_Balance</b> method sets the balance. This method is not implemented for terminals shipped with TAPI 3.0 and higher.

## -parameters

### -param lBalance [in]

Balance.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Terminal's balance methods are not implemented.

</td>
</tr>
</table>

## -remarks

The balance property is a value between –10,000 and 10,000. A value of –10,000 indicates that the right speaker has been disabled and only the left speaker is receiving an audio signal. A value of 0 indicates that both speakers are receiving equivalent audio signals. A value of 10,000 indicates that the left speaker has been disabled and only the right speaker is receiving an audio signal.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal">ITBasicAudioTerminal</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance">get_Balance</a>
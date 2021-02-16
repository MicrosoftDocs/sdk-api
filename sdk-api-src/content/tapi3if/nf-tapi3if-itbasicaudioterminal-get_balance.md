---
UID: NF:tapi3if.ITBasicAudioTerminal.get_Balance
title: ITBasicAudioTerminal::get_Balance (tapi3if.h)
description: The get_Balance method gets the balance. This method is not implemented for terminals shipped with TAPI 3.0 and higher.
helpviewer_keywords: ["ITBasicAudioTerminal interface [TAPI 2.2]","get_Balance method","ITBasicAudioTerminal.get_Balance","ITBasicAudioTerminal::get_Balance","_tapi3_itbasicaudioterminal_get_balance","get_Balance","get_Balance method [TAPI 2.2]","get_Balance method [TAPI 2.2]","ITBasicAudioTerminal interface","tapi3.itbasicaudioterminal_get_balance","tapi3if/ITBasicAudioTerminal::get_Balance"]
old-location: tapi3\itbasicaudioterminal_get_balance.htm
tech.root: tapi3
ms.assetid: 36aff613-6065-4d92-98e7-3e5b851bf544
ms.date: 12/05/2018
ms.keywords: ITBasicAudioTerminal interface [TAPI 2.2],get_Balance method, ITBasicAudioTerminal.get_Balance, ITBasicAudioTerminal::get_Balance, _tapi3_itbasicaudioterminal_get_balance, get_Balance, get_Balance method [TAPI 2.2], get_Balance method [TAPI 2.2],ITBasicAudioTerminal interface, tapi3.itbasicaudioterminal_get_balance, tapi3if/ITBasicAudioTerminal::get_Balance
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
 - ITBasicAudioTerminal::get_Balance
 - tapi3if/ITBasicAudioTerminal::get_Balance
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
 - ITBasicAudioTerminal.get_Balance
---

# ITBasicAudioTerminal::get_Balance


## -description

The 
<b>get_Balance</b> method gets the balance. This method is not implemented for terminals shipped with TAPI 3.0 and higher.

## -parameters

### -param plBalance [out]

Pointer to balance.

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
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Terminal does not support balance operations.

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



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance">put_Balance</a>
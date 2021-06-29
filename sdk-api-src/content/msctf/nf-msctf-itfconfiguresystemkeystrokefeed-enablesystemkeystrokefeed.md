---
UID: NF:msctf.ITfConfigureSystemKeystrokeFeed.EnableSystemKeystrokeFeed
title: ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed (msctf.h)
description: ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed method
helpviewer_keywords: ["EnableSystemKeystrokeFeed","EnableSystemKeystrokeFeed method [Text Services Framework]","EnableSystemKeystrokeFeed method [Text Services Framework]","ITfConfigureSystemKeystrokeFeed interface","ITfConfigureSystemKeystrokeFeed interface [Text Services Framework]","EnableSystemKeystrokeFeed method","ITfConfigureSystemKeystrokeFeed.EnableSystemKeystrokeFeed","ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed","_tsf_itfconfiguresystemkeystrokefeed_enablesystemkeystrokefeed_ref","msctf/ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed","tsf.itfconfiguresystemkeystrokefeed_enablesystemkeystrokefeed"]
old-location: tsf\itfconfiguresystemkeystrokefeed_enablesystemkeystrokefeed.htm
tech.root: TSF
ms.assetid: 66dc5db3-c4d9-422e-bbc0-300409a9576a
ms.date: 12/05/2018
ms.keywords: EnableSystemKeystrokeFeed, EnableSystemKeystrokeFeed method [Text Services Framework], EnableSystemKeystrokeFeed method [Text Services Framework],ITfConfigureSystemKeystrokeFeed interface, ITfConfigureSystemKeystrokeFeed interface [Text Services Framework],EnableSystemKeystrokeFeed method, ITfConfigureSystemKeystrokeFeed.EnableSystemKeystrokeFeed, ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed, _tsf_itfconfiguresystemkeystrokefeed_enablesystemkeystrokefeed_ref, msctf/ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed, tsf.itfconfiguresystemkeystrokefeed_enablesystemkeystrokefeed
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed
 - msctf/ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfConfigureSystemKeystrokeFeed.EnableSystemKeystrokeFeed
---

# ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed


## -description

Enables the TSF manager to process keystrokes after being disabled by DisableSystemKeystrokeFeed.



## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
There was no corresponding call to DisableSystemKeystrokeFeed.

</td>
</tr>
</table>

## -remarks

By default, the TSF manager will process keystrokes and pass them to the text services. An application prevents this by calling <b>DisableSystemKeystrokeFeed</b> .

Calls to <b>DisableSystemKeystrokeFeed</b> are cumulative, so every call to <b>DisableSystemKeystrokeFeed</b> requires a subsequent call to <b>EnableSystemKeystrokeFeed</b>. Calling <b>EnableSystemKeystrokeFeed</b> will not enable keystroke processing if <b>DisableSystemKeystrokeFeed</b> is called more than once.

## -see-also

[ITfConfigureSystemKeystrokeFeed interface](nn-msctf-itfconfiguresystemkeystrokefeed.md), [ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed](nf-msctf-itfconfiguresystemkeystrokefeed-disablesystemkeystrokefeed.md)


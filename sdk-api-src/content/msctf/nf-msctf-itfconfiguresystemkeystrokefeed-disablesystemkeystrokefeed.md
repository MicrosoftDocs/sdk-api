---
UID: NF:msctf.ITfConfigureSystemKeystrokeFeed.DisableSystemKeystrokeFeed
title: ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed (msctf.h)
description: ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed method
helpviewer_keywords: ["DisableSystemKeystrokeFeed","DisableSystemKeystrokeFeed method [Text Services Framework]","DisableSystemKeystrokeFeed method [Text Services Framework]","ITfConfigureSystemKeystrokeFeed interface","ITfConfigureSystemKeystrokeFeed interface [Text Services Framework]","DisableSystemKeystrokeFeed method","ITfConfigureSystemKeystrokeFeed.DisableSystemKeystrokeFeed","ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed","_tsf_itfconfiguresystemkeystrokefeed_disablesystemkeystrokefeed_ref","msctf/ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed","tsf.itfconfiguresystemkeystrokefeed_disablesystemkeystrokefeed"]
old-location: tsf\itfconfiguresystemkeystrokefeed_disablesystemkeystrokefeed.htm
tech.root: TSF
ms.assetid: 6bdca5cc-84b4-4184-a8cc-76dddc573b35
ms.date: 12/05/2018
ms.keywords: DisableSystemKeystrokeFeed, DisableSystemKeystrokeFeed method [Text Services Framework], DisableSystemKeystrokeFeed method [Text Services Framework],ITfConfigureSystemKeystrokeFeed interface, ITfConfigureSystemKeystrokeFeed interface [Text Services Framework],DisableSystemKeystrokeFeed method, ITfConfigureSystemKeystrokeFeed.DisableSystemKeystrokeFeed, ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed, _tsf_itfconfiguresystemkeystrokefeed_disablesystemkeystrokefeed_ref, msctf/ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed, tsf.itfconfiguresystemkeystrokefeed_disablesystemkeystrokefeed
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
 - ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed
 - msctf/ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed
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
 - ITfConfigureSystemKeystrokeFeed.DisableSystemKeystrokeFeed
---

# ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed


## -description

Prevents the TSF manager from processing keystrokes.



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
</table>

## -remarks

By default, the TSF manager will process keystrokes and pass them to the text services. An application prevents this by calling this method. Typically, this method is called when text service input is inappropriate, for example when a menu is displayed.

Calls to this method are cumulative, so every call to this method requires a subsequent call to <a href="/windows/desktop/api/msctf/nf-msctf-itfconfiguresystemkeystrokefeed-enablesystemkeystrokefeed">ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed</a>.

## -see-also

[ITfConfigureSystemKeystrokeFeed interface](nn-msctf-itfconfiguresystemkeystrokefeed.md), [ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed](nf-msctf-itfconfiguresystemkeystrokefeed-enablesystemkeystrokefeed.md)

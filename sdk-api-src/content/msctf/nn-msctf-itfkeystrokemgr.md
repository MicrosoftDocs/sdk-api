---
UID: NN:msctf.ITfKeystrokeMgr
title: ITfKeystrokeMgr (msctf.h)
description: The ITfKeystrokeMgr interface is implemented by the TSF manager and used by applications and text services to interact with the keyboard manager.
old-location: tsf\itfkeystrokemgr.htm
tech.root: TSF
ms.assetid: 93c1591d-2c95-45cb-8fc5-5726e905f202
ms.date: 12/05/2018
ms.keywords: ITfKeystrokeMgr, ITfKeystrokeMgr interface [Text Services Framework], ITfKeystrokeMgr interface [Text Services Framework],described, _tsf_itfkeystrokemgr_ref, msctf/ITfKeystrokeMgr, tsf.itfkeystrokemgr
f1_keywords:
- msctf/ITfKeystrokeMgr
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITfKeystrokeMgr
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfKeystrokeMgr interface


## -description


The <b>ITfKeystrokeMgr</b> interface is implemented by the TSF manager and used by applications and text services to interact with the keyboard manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfKeystrokeMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfKeystrokeMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfKeystrokeMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-advisekeyeventsink">AdviseKeyEventSink</a>
</td>
<td align="left" width="63%">
Installs a key event sink to receive keyboard events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-getforeground">GetForeground</a>
</td>
<td align="left" width="63%">
Obtains the class identifier of the foreground TSF text service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-getpreservedkey">GetPreservedKey</a>
</td>
<td align="left" width="63%">
Obtains the command GUID for a preserved key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-getpreservedkeydescription">GetPreservedKeyDescription</a>
</td>
<td align="left" width="63%">
Obtains the description string of an existing preserved key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-ispreservedkey">IsPreservedKey</a>
</td>
<td align="left" width="63%">
Determines if a command GUID and key combination is a preserved key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-keydown">KeyDown</a>
</td>
<td align="left" width="63%">
Passes a key down event to the keystroke manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-keyup">KeyUp</a>
</td>
<td align="left" width="63%">
Passes a key up event to the keystroke manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-preservekey">PreserveKey</a>
</td>
<td align="left" width="63%">
Registers a preserved key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-setpreservedkeydescription">SetPreservedKeyDescription</a>
</td>
<td align="left" width="63%">
Modifies the description string of an existing preserved key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-simulatepreservedkey">SimulatePreservedKey</a>
</td>
<td align="left" width="63%">
Simulates the execution of a preserved key sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-testkeydown">TestKeyDown</a>
</td>
<td align="left" width="63%">
Determines if the keystroke manager will handle a key down event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-testkeyup">TestKeyUp</a>
</td>
<td align="left" width="63%">
Determines if the keystroke manager will handle a key up event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-unadvisekeyeventsink">UnadviseKeyEventSink</a>
</td>
<td align="left" width="63%">
Removes a key event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-unpreservekey">UnpreserveKey</a>
</td>
<td align="left" width="63%">
Unregisters a preserved key.

</td>
</tr>
</table> 


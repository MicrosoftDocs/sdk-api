---
UID: NN:msctf.ITfMouseTracker
title: ITfMouseTracker (msctf.h)
description: The ITfMouseTracker interface is implemented by the TSF manager and is used by a text service to manage mouse event notification sinks. An instance of this interface is obtained by querying an ITfContext object for IID_ITfMouseTracker.
helpviewer_keywords: ["ITfMouseTracker","ITfMouseTracker interface [Text Services Framework]","ITfMouseTracker interface [Text Services Framework]","described","_tsf_itfmousetracker_ref","msctf/ITfMouseTracker","tsf.itfmousetracker"]
old-location: tsf\itfmousetracker.htm
tech.root: TSF
ms.assetid: aad07b35-99e0-4c76-ba65-93c2c972303d
ms.date: 12/05/2018
ms.keywords: ITfMouseTracker, ITfMouseTracker interface [Text Services Framework], ITfMouseTracker interface [Text Services Framework],described, _tsf_itfmousetracker_ref, msctf/ITfMouseTracker, tsf.itfmousetracker
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITfMouseTracker
 - msctf/ITfMouseTracker
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
 - ITfMouseTracker
---

# ITfMouseTracker interface


## -description

The <b>ITfMouseTracker</b> interface is implemented by the TSF manager and is used by a text service to manage mouse event notification sinks. An instance of this interface is obtained by querying an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> object for IID_ITfMouseTracker.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMouseTracker</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfMouseTracker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfMouseTracker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfmousetracker-advisemousesink">AdviseMouseSink</a>
</td>
<td align="left" width="63%">
Installs a mouse event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfmousetracker-unadvisemousesink">UnadviseMouseSink</a>
</td>
<td align="left" width="63%">
Uninstalls a mouse event sink.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>


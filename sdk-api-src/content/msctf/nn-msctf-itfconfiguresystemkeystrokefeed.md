---
UID: NN:msctf.ITfConfigureSystemKeystrokeFeed
title: ITfConfigureSystemKeystrokeFeed (msctf.h)
author: windows-sdk-content
description: The ITfConfigureSystemKeystrokeFeed interface is implemented by the TSF manager to enable and disable the processing of keystrokes.
old-location: tsf\itfconfiguresystemkeystrokefeed.htm
tech.root: TSF
ms.assetid: 9b15d628-87aa-4e20-b9c3-fb29a79683cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfConfigureSystemKeystrokeFeed, ITfConfigureSystemKeystrokeFeed interface [Text Services Framework], ITfConfigureSystemKeystrokeFeed interface [Text Services Framework],described, _tsf_itfconfiguresystemkeystrokefeed_ref, msctf/ITfConfigureSystemKeystrokeFeed, tsf.itfconfiguresystemkeystrokefeed
ms.topic: interface
f1_keywords: 
 - "msctf/ITfConfigureSystemKeystrokeFeed"
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
 - ITfConfigureSystemKeystrokeFeed
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfConfigureSystemKeystrokeFeed interface


## -description


The <b>ITfConfigureSystemKeystrokeFeed</b> interface is implemented by the TSF manager to enable and disable the processing of keystrokes. This interface is obtained by calling the TSF manager's <b>ITfThreadMgr::QueryInterface</b> with IID_ITfConfigureSystemKeystrokeFeed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfConfigureSystemKeystrokeFeed</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfConfigureSystemKeystrokeFeed</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfConfigureSystemKeystrokeFeed</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfconfiguresystemkeystrokefeed-disablesystemkeystrokefeed">DisableSystemKeystrokeFeed</a>
</td>
<td align="left" width="63%">
Prevents the TSF manager from processing keystrokes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfconfiguresystemkeystrokefeed-enablesystemkeystrokefeed">EnableSystemKeystrokeFeed</a>
</td>
<td align="left" width="63%">
Enables the TSF manager to process keystrokes after being disabled by DisableSystemKeystrokeFeed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 


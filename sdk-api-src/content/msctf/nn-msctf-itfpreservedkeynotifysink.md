---
UID: NN:msctf.ITfPreservedKeyNotifySink
title: ITfPreservedKeyNotifySink (msctf.h)
author: windows-sdk-content
description: The ITfPreservedKeyNotifySink interface is implemented by an application or TSF text service to receive notifications when keys are preserved, unpreserved, or when a preserved key description changes.
old-location: tsf\itfpreservedkeynotifysink.htm
tech.root: TSF
ms.assetid: 0bf786b5-efcd-4c58-835b-47e7adf9be63
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfPreservedKeyNotifySink, ITfPreservedKeyNotifySink interface [Text Services Framework], ITfPreservedKeyNotifySink interface [Text Services Framework],described, _tsf_itfpreservedkeynotifysink_ref, msctf/ITfPreservedKeyNotifySink, tsf.itfpreservedkeynotifysink
ms.topic: interface
f1_keywords: ["msctf/ITfPreservedKeyNotifySink"]
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
 - ITfPreservedKeyNotifySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfPreservedKeyNotifySink interface


## -description


The <b>ITfPreservedKeyNotifySink</b> interface is implemented by an application or TSF text service to receive notifications when keys are preserved, unpreserved, or when a preserved key description changes. This advise sink is installed by calling the TSF manager <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfPreservedKeyNotifySink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfPreservedKeyNotifySink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfPreservedKeyNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfPreservedKeyNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpreservedkeynotifysink-onupdated">OnUpdated</a>
</td>
<td align="left" width="63%">
Called when a key is preserved, unpreserved, or when a preserved key description changes.

</td>
</tr>
</table> 


## -remarks



Preserved keys are keyboard shortcuts that an application or TSF text service can register with the TSF manager.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-preservekey">ITfKeystrokeMgr::PreserveKey
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-setpreservedkeydescription">ITfKeystrokeMgr::SetPreservedKeyDescription
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfkeystrokemgr-unpreservekey">ITfKeystrokeMgr::UnpreserveKey
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 


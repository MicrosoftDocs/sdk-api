---
UID: NN:msctf.ITfTextEditSink
title: ITfTextEditSink
author: windows-sdk-content
description: The ITfTextEditSink interface supports completion of an edit session that involves read/write access.
old-location: tsf\itftexteditsink.htm
tech.root: TSF
ms.assetid: 50f44525-eb3a-4db2-90c2-3e0c6c6146e3
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITfTextEditSink, ITfTextEditSink interface [Text Services Framework], ITfTextEditSink interface [Text Services Framework],described, _tsf_itftexteditsink_ref, msctf/ITfTextEditSink, tsf.itftexteditsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.dll: Imekrcic.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfTextEditSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfTextEditSink interface


## -description


The <b>ITfTextEditSink</b> interface supports completion of an edit session that involves read/write access. Install this advise sink by calling <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ITfTextEditSink. A text service or application can optionally implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfTextEditSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfTextEditSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfTextEditSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7763a879-a558-463d-837b-e38e6f84b9f7">OnEndEdit</a>
</td>
<td align="left" width="63%">
Receives a notification upon completion of an ITfEditSession::DoEditSession method that has read/write access to the context.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/6c7b150c-0ca0-4aa5-8828-0c548dbfb215">ITfContext::RequestEditSession
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 


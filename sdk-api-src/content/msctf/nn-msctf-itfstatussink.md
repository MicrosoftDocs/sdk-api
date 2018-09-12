---
UID: NN:msctf.ITfStatusSink
title: ITfStatusSink
author: windows-sdk-content
description: The ITfStatusSink interface supports changes to the global document status. This advise sink is installed by calling ITfSource::AdviseSink with IID_ITfStatusSink. A text service can optionally implement this interface.
old-location: tsf\itfstatussink.htm
tech.root: TSF
ms.assetid: 5fc37251-938b-4581-bb54-816749b17001
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfStatusSink, ITfStatusSink interface [Text Services Framework], ITfStatusSink interface [Text Services Framework],described, _tsf_itfstatussink_ref, msctf/ITfStatusSink, tsf.itfstatussink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.dll: Tiptsf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfStatusSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfStatusSink interface


## -description


The <b>ITfStatusSink</b> interface supports changes to the global document status. This advise sink is installed by calling <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ITfStatusSink. A text service can optionally implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfStatusSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfStatusSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfStatusSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6eabf08f-006b-43b4-aea7-1d803b3d09b2">OnStatusChange</a>
</td>
<td align="left" width="63%">
Receives a notification when one of the dynamic flags of the TF_STATUS structure changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/1f00c8e1-435c-45ce-892a-36af68154144">TF_STATUS
      </a>
 

 


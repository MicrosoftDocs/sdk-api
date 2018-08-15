---
UID: NN:msctf.ITfCleanupContextDurationSink
title: ITfCleanupContextDurationSink
author: windows-sdk-content
description: The ITfCleanupContextDurationSink interface is implemented by a text service to receive notifications when a context cleanup operation is performed.
old-location: tsf\itfcleanupcontextdurationsink.htm
old-project: TSF
ms.assetid: 2bbdc26a-5543-4de4-b347-2062be593c4b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfCleanupContextDurationSink, ITfCleanupContextDurationSink interface [Text Services Framework], ITfCleanupContextDurationSink interface [Text Services Framework],described, _tsf_itfcleanupcontextdurationsink_ref, msctf/ITfCleanupContextDurationSink, tsf.itfcleanupcontextdurationsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfCleanupContextDurationSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCleanupContextDurationSink interface


## -description


The <b>ITfCleanupContextDurationSink</b> interface is implemented by a text service to receive notifications when a context cleanup operation is performed. This notification sink is installed by calling <a href="https://msdn.microsoft.com/d9231f36-24c4-4d46-97e7-518f5fcc1ce2">ITfSourceSingle::AdviseSingleSink</a> with IID_ITfCleanupContextDurationSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCleanupContextDurationSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCleanupContextDurationSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCleanupContextDurationSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7af4584-9c77-40cd-a83d-7b6fd3945b17">OnEndCleanupContext</a>
</td>
<td align="left" width="63%">
Called when a context cleanup operation completes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a35aa7b1-273d-47ff-a705-298393f4abd2">OnStartCleanupContext</a>
</td>
<td align="left" width="63%">
Called when a context cleanup operation is about to begin.

</td>
</tr>
</table> 


## -remarks



A context cleanup occurs when:

<ul>
<li>The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.</li>
<li>
<a href="https://msdn.microsoft.com/7293fbfa-c385-4713-80b2-760e54dbf4c1">ITfThreadMgr::Deactivate
            </a> is called while a context is still on the context stack.</li>
</ul>
A text service can use the notifications of this interface to prevent itself from performing any context initialization during the context cleanup operation.




## -see-also




<a href="https://msdn.microsoft.com/d9231f36-24c4-4d46-97e7-518f5fcc1ce2">ITfSourceSingle::AdviseSingleSink
      </a>



<a href="https://msdn.microsoft.com/7293fbfa-c385-4713-80b2-760e54dbf4c1">ITfThreadMgr::Deactivate
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 


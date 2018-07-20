---
UID: NN:msctf.ITfPreservedKeyNotifySink
title: ITfPreservedKeyNotifySink
author: windows-sdk-content
description: The ITfPreservedKeyNotifySink interface is implemented by an application or TSF text service to receive notifications when keys are preserved, unpreserved, or when a preserved key description changes.
old-location: tsf\itfpreservedkeynotifysink.htm
old-project: TSF
ms.assetid: 0bf786b5-efcd-4c58-835b-47e7adf9be63
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfPreservedKeyNotifySink, ITfPreservedKeyNotifySink interface [Text Services Framework], ITfPreservedKeyNotifySink interface [Text Services Framework],described, _tsf_itfpreservedkeynotifysink_ref, msctf/ITfPreservedKeyNotifySink, tsf.itfpreservedkeynotifysink
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfPreservedKeyNotifySink interface


## -description


The <b>ITfPreservedKeyNotifySink</b> interface is implemented by an application or TSF text service to receive notifications when keys are preserved, unpreserved, or when a preserved key description changes. This advise sink is installed by calling the TSF manager <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ITfPreservedKeyNotifySink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfPreservedKeyNotifySink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfPreservedKeyNotifySink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/50654da7-60ee-4038-a02a-1055445f1e5d">OnUpdated</a>
</td>
<td align="left" width="63%">
Called when a key is preserved, unpreserved, or when a preserved key description changes.

</td>
</tr>
</table> 


## -remarks



Preserved keys are keyboard shortcuts that an application or TSF text service can register with the TSF manager.




## -see-also




<a href="https://msdn.microsoft.com/ad5cd485-9231-4c29-8977-754dbf25c979">
        ITfKeystrokeMgr::PreserveKey
      </a>



<a href="https://msdn.microsoft.com/feb83f22-652c-4fec-b35d-a0cc41eab533">
        ITfKeystrokeMgr::SetPreservedKeyDescription
      </a>



<a href="https://msdn.microsoft.com/05975fce-04c3-4316-a9b2-ed015e7aa8fe">
        ITfKeystrokeMgr::UnpreserveKey
      </a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 


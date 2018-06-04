---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITfCleanupContextDurationSink::OnEndCleanupContext


## -description




## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A context cleanup occurs when:

<ul>
<li>The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.</li>
<li>
<a href="https://msdn.microsoft.com/7293fbfa-c385-4713-80b2-760e54dbf4c1">
              ITfThreadMgr::Deactivate
            </a> is called while a context is still on the context stack.</li>
</ul>

<a href="https://msdn.microsoft.com/a35aa7b1-273d-47ff-a705-298393f4abd2">ITfCleanupContextDurationSink::OnStartCleanupContext
        </a> is called just before the TSF manager begins making <a href="https://msdn.microsoft.com/6af597e6-f997-4b28-8994-a8dbabcaaa68">ITfCleanupContextSink::OnCleanupContext</a> notifications. When all of the OnCleanupContext notifications complete, the TSF manager calls <b>OnEndCleanupContext</b>.




## -see-also




<a href="https://msdn.microsoft.com/2bbdc26a-5543-4de4-b347-2062be593c4b">ITfCleanupContextDurationSink</a>



<a href="https://msdn.microsoft.com/a35aa7b1-273d-47ff-a705-298393f4abd2">ITfCleanupContextDurationSink::OnStartCleanupContext
      </a>



<a href="https://msdn.microsoft.com/6af597e6-f997-4b28-8994-a8dbabcaaa68">
        ITfCleanupContextSink::OnCleanupContext
      </a>
 

 


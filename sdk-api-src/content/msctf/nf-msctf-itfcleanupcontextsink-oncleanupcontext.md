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

# ITfCleanupContextSink::OnCleanupContext


## -description




## -parameters




### -param ecWrite [in]

Contains a <a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">TfEditCookie</a> value that identifies the edit context cleaned up. The edit context is guaranteed to have a read/write lock.


### -param pic [in]

Pointer to an <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface that represents the context cleaned up.


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
This method provides the text service with a final opportunity to modify the text or properties within the context. For example, if the text service currently has a composition open when the context cleanup occurs. This method enables the text service to close the composition before the context is destroyed.

The TSF manager automatically releases all properties, including custom properties, when a context is removed from the context stack. Therefore, it is unnecessary for a text service to release its properties in response to this event.




## -see-also




<a href="https://msdn.microsoft.com/f88ebef7-2796-4076-892f-28fac6e143de">ITfCleanupContextSink</a>



<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">
        ITfContext
      </a>



<a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">TfEditCookie
      </a>
 

 


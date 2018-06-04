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

# ITfTextEditSink::OnEndEdit


## -description




## -parameters




### -param pic [in]

Pointer to the <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface for the edited context.


### -param ecReadOnly [in]

Specifies a <a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">TfEditCookie</a> value for read-only access to the context.


### -param pEditRecord [in]

Pointer to the <a href="https://msdn.microsoft.com/2106cd97-9e1f-4d7c-a7a4-55676cf8923b">ITfEditRecord</a> interface used to access the modifications to the context.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An edit session with read/write access is requested with a call to the <a href="https://msdn.microsoft.com/6c7b150c-0ca0-4aa5-8828-0c548dbfb215">ITfContext::RequestEditSession</a> method using the TF_ES_READWRITE flag, which establishes an <b>ITfEditSession::DoEditSession</b> method to perform the session. When such a <b>ITfEditSession::DoEditSession</b> method completes, TSF calls this method.

A text service can use the <i>ecReadOnly</i> parameter only to view the context. If changes are required, the text service must use an asynchronous call to the <b>ITfContext::RequestEditSession</b> method. However, a text service should modify only text that it previously entered as part of a composition. Otherwise, two or more text services could repeatedly modify the same text. A text service can use the <a href="https://msdn.microsoft.com/88a8a2c1-bd5f-47d2-8612-c7e0cabfe254">ITfContext::InWriteSession</a> method to determine if it performed the completed edit session.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/88a8a2c1-bd5f-47d2-8612-c7e0cabfe254">
        ITfContext::InWriteSession
      </a>



<a href="https://msdn.microsoft.com/6c7b150c-0ca0-4aa5-8828-0c548dbfb215">
        ITfContext::RequestEditSession
      </a>



<a href="https://msdn.microsoft.com/2106cd97-9e1f-4d7c-a7a4-55676cf8923b">
        ITfEditRecord
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/50f44525-eb3a-4db2-90c2-3e0c6c6146e3">ITfTextEditSink</a>



<a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">
        TfEditCookie
      </a>
 

 


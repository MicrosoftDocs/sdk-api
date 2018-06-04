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

# ITfThreadMgrEventSink::OnSetFocus


## -description




## -parameters




### -param pdimFocus [in]

Pointer to the document manager receiving the input focus. If no document is receiving the focus, this will be <b>NULL</b>.


### -param pdimPrevFocus [in]

Pointer to the document manager that previously had the input focus. If no document had the focus, this will be <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b437c646-2a15-4ad6-8e7e-3553e7106249">ITfThreadMgr::SetFocus
      </a>



<a href="https://msdn.microsoft.com/be2a3eb1-cb17-4d8b-a44d-ccb33749c8f6">ITfThreadMgrEventSink</a>
 

 


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

# ITfStatusSink::OnStatusChange


## -description




## -parameters




### -param pic [in]

Pointer to the <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface whose status has changed.


### -param dwFlags [in]

Indicates that one of the dynamic flags changed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method receives a callback when one of the flags of the <b>dwDynamicFlags</b> member of the <b>TF_STATUS</b> structure changes value. To obtain the changed flag(s), use the <a href="https://msdn.microsoft.com/a1f193b0-fcfc-4db6-90e9-61d528b08672">ITfContext::GetStatus</a> method.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">
        ITfContext
      </a>



<a href="https://msdn.microsoft.com/a1f193b0-fcfc-4db6-90e9-61d528b08672">
        ITfContext::GetStatus
      </a>



<a href="https://msdn.microsoft.com/5fc37251-938b-4581-bb54-816749b17001">ITfStatusSink</a>



<a href="https://msdn.microsoft.com/1f00c8e1-435c-45ce-892a-36af68154144">TF_STATUS
      </a>
 

 


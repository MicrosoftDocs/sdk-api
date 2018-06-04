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

# ITfTextLayoutSink::OnLayoutChange


## -description




## -parameters




### -param pic [in]

Pointer to the <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface for the context that changed.


### -param lcode [in]

Specifies the <a href="https://msdn.microsoft.com/b9ff6d11-68f2-47c5-b8d7-b3bc2533fdbb">TfLayoutCode</a> element that describes the layout change.


### -param pView [in]

Pointer to the <a href="https://msdn.microsoft.com/302d185d-dab7-4a77-a5cf-da2529d8b24a">ITfContextView</a> interface for the context view in that the layout change occurred.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each context has a default view for which a reference can be obtained using the <a href="https://msdn.microsoft.com/41f7eb74-bca2-4d53-8a70-0b872616fd1b">ITfContext::GetActiveView</a> method. The method returns only the value TF_LC_CHANGE for the <i>lcode</i> parameter for this view, because the values are possible only for multiple views. Because TSF does not support multiple views, this method never receives other values of the <b>TfLayoutCode</b> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/41f7eb74-bca2-4d53-8a70-0b872616fd1b">
        ITfContext::GetActiveView
      </a>



<a href="https://msdn.microsoft.com/302d185d-dab7-4a77-a5cf-da2529d8b24a">
        ITfContextView
      </a>



<a href="https://msdn.microsoft.com/370e30a8-6eed-448a-87c7-7fd01e9973c6">
        ITfTextLayoutSink
      </a>



<a href="https://msdn.microsoft.com/b9ff6d11-68f2-47c5-b8d7-b3bc2533fdbb">
        TfLayoutCode
      </a>
 

 


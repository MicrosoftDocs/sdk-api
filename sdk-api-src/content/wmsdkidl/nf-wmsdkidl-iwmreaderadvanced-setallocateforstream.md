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

# IWMReaderAdvanced::SetAllocateForStream


## -description



The <b>SetAllocateForStream</b> method specifies whether the reader uses <a href="https://msdn.microsoft.com/82d31f4b-d8a8-4538-be5e-dd9149e3f420">IWMReaderCallbackAdvanced::AllocateForStream</a> to allocate buffers for stream samples.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.


### -param fAllocate [in]

Boolean value that is True if the reader uses <b>IWMReaderCallbackAdvanced</b> to allocate streams.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



If the application's callback implements the <a href="https://msdn.microsoft.com/be727c7b-b252-44db-825b-5c683e551fd2">IWMReaderAllocatorEx</a> interface interface, the <a href="https://msdn.microsoft.com/bb12f0e1-dc9c-447e-a28d-30c45eb95d09">AllocateForStreamEx</a> method is called instead of <b>AllocateForStream</b>.




## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/816f13b1-9856-482d-b5b1-4aaf5c61c230">IWMReaderAdvanced::GetAllocateForStream</a>



<a href="https://msdn.microsoft.com/bb12f0e1-dc9c-447e-a28d-30c45eb95d09">IWMReaderAllocatorEx::AllocateForStreamEx</a>
 

 


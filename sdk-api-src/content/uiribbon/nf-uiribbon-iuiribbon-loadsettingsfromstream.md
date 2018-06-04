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

# IUIRibbon::LoadSettingsFromStream


## -description



			Reads ribbon settings from a binary stream.
		


## -parameters




### -param pStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>


					Pointer to an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object. 
				


## -returns



Type: <b>HRESULT</b>


						Returns S_OK if successful, or E_FAIL if the format or content of the serialized stream 
						is empty or cannot be verified by the Ribbon framework.
					




## -remarks




				The stream is supplied by the host application.
			
				If the Windows Ribbon framework is unable to load a valid stream, the default ribbon layout is rendered instead.
			


				The <b>LoadSettingsFromStream </b> method is useful for persisting ribbon state, such as Quick Access Toolbar (QAT) items, across application instances. 
			




## -see-also




<a href="https://msdn.microsoft.com/6a43f17b-dbf6-4c5b-818f-c0dde896de99">IUIRibbon</a>



<a href="https://msdn.microsoft.com/b5cd7cfd-95b7-49a1-8931-8befef7d4298">IUIRibbon::SaveSettingsToStream</a>



<a href="https://msdn.microsoft.com/f59e36be-8e3d-454a-b93c-9fc5fc5ecb47">Persisting Ribbon State</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 


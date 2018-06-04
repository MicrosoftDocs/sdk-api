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

# ISettingsEngine::LoadStore


## -description


 Initializes and loads the schema store hive. 


## -parameters




### -param Flags [in]

Flags must have a value 0 or have the value <b>LINK_STORE_TO_ENGINE_INSTANCE</b>. In a normal operation, loading the store is a persistent operation which affects the overall state of the system. The store is not cleaned up after the process exits. The developer must call <a href="https://msdn.microsoft.com/10c0e5c7-41df-4ebb-86be-0c2c6e013849">UnloadStore</a> to avoid a leak in the hive. A leak in the hive can cause future issues when accessing the same image.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -remarks



<div class="alert"><b>Note</b>  If the flag <b>LINK_STORE_TO_ENGINE_INSTANCE</b> is passed as an input parameter, the loaded store is considered attached to the current engine and will be unloaded when the <a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a> object on which this method was called is finalized. The <b>ISettingsEngine</b> object can be finalized either by releasing all pointers to it, or by terminating the process. Developers can call <a href="https://msdn.microsoft.com/10c0e5c7-41df-4ebb-86be-0c2c6e013849">UnloadStore</a> to force the store to be unloaded early, but it is not necessary when this flag is used.</div>
<div> </div>
<div class="alert"><b>Note</b>  When using a target; that is, if you are not loading the store from the default file to the default location in the registry, you must call <a href="https://msdn.microsoft.com/10c0e5c7-41df-4ebb-86be-0c2c6e013849">UnloadStore</a> to verify that you do not lock the file.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a>
 

 


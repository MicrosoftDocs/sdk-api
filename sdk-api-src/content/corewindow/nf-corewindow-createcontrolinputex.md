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

# CreateControlInputEx function


## -description


Creates a <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a> object in a worker thread or the UI thread. 


## -parameters




### -param pCoreWindow [in]

Pointer to the parent <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> to which the <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a> object will be attached. This parameter can’t be NULL.


### -param riid [in]

Interface ID of the object. Must to be set to the UUID for  <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a>, which is 9F488807-4580-4BE8-BE68-92A9311713BB.


### -param ppv [out]

Pointer to receive the <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a> object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This API must be called from the UI thread or worker thread to create <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a> object. The object created using this API can be used only in that thread in which it was created. 

If the call is successful, the  caller can call <b>QueryInterface</b> on the returned <a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a> object to obtain the <a href="https://msdn.microsoft.com/F7BA7EFB-D9DC-4FF2-97A4-C4818BCBD599">ICoreInputInterop</a> object that created it.

This API will fail if the following scenarios occur:

<ul>
<li>The <i>pCoreWindow</i> parameter is <b>NULL</b>.</li>
<li>If the <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> passed is not same as the <b>CoreWindow</b> present in the calling thread. </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/675ca745-c593-4714-9fae-5fcab2c0336e">ICoreInputSourceBase</a>
 

 


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

# IMFPMPHost::CreateObjectByCLSID


## -description



          Creates an object in the protect media path (PMP) process, from a CLSID.
        


## -parameters




### -param clsid [in]


            The CLSID of the object to create.
          


### -param pStream [in]

A pointer to the <b>IStream</b> interface. This parameter can be <b>NULL</b>. If this parameter is not <b>NULL</b>, the PMP host queries the created object for the <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> interface and calls <b>IPersistStream::Load</b>, passing in the <i>pStream</i> pointer.
          


### -param riid [in]


            The interface identifier (IID) of the interface to retrieve.
          


### -param ppv [out]


            Receives a pointer to the requested interface. The caller must release the interface.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        You can use the <i>pStream</i> parameter to initialize the object after it is created.
      




## -see-also




<a href="https://msdn.microsoft.com/fab1fb42-07c5-4a74-b6f5-0950b2c3ba46">IMFPMPHost</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 


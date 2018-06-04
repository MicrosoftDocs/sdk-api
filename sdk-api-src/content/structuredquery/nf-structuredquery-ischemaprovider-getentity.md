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

# ISchemaProvider::GetEntity


## -description



      Retrieves an entity by name from the loaded schema. 


## -parameters




### -param pszEntityName [in]

Type: <b>LPCWSTR</b>


          The name of the entity being requested.
        


### -param pEntity [out, retval]

Type: <b><a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a>**</b>


          Receives the address of a pointer to the requested entity. The calling application must release the entity by calling its <a href="_com_IUnknown_Release">IUnknown::Release</a> method. If there is no entity with the specified name, this parameter is set to <b>NULL</b>.
        


## -returns



Type: <b>HRESULT</b>


          Returns S_OK if successful, S_FALSE if there is no entity with the specified name, or an error value otherwise.
        




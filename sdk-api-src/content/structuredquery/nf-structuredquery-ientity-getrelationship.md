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

# IEntity::GetRelationship


## -description



          Retrieves the <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a> object for this entity as requested by name.
        


## -parameters




### -param pszRelationName [in]

Type: <b>LPCWSTR</b>


                The name of the relationship to find.
            


### -param pRelationship [out, retval]

Type: <b><a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a>**</b>


                Receives the address of a pointer to the requested <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a> object, or <b>NULL</b> if this entity has no relationship with the name specified.
            


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there is no matching relationship, or an error value otherwise.




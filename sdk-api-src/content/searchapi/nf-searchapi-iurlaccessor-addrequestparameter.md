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

# IUrlAccessor::AddRequestParameter


## -description



            Requests a property-value set. 
        


## -parameters




### -param pSpec [in]

Type: <b><a href="_stg_propspec">PROPSPEC</a>*</b>


                Pointer to a <a href="_stg_propspec">PROPSPEC</a> structure containing the requested property.
                


### -param pVar [in]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>


                Pointer to a <a href="_stg_propvariant">PROPVARIANT</a> structure containing the value for the property specified by <i>pSpec</i>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Implement this method to obtain additional information from the content source (for instance, the If-Modified-Since header in an HTTP request).
            




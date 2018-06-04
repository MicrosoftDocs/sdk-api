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

# ISearchNotifyInlineSite::OnCatalogStatusChange


## -description



            Called by the search service to notify a client when the status of the catalog changes.
        


## -parameters




### -param guidCatalogResetSignature [in]

Type: <b>REFGUID</b>


                    A GUID representing the catalog reset. If this GUID changes, all notifications must be resent.
                


### -param guidCheckPointSignature [in]

Type: <b>REFGUID</b>


                    A GUID representing the last checkpoint restored. If this GUID changes, all notifications accumulated since the last saved checkpoint must be resent.
                


### -param dwLastCheckPointNumber [in]

Type: <b>DWORD</b>

A number indicating the last checkpoint saved. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




                When a catalog checkpoint occurs, the search service updates the <i>dwLastCheckPointNumber</i>, and all notifications sent prior to that checkpoint are safe and recoverable in the event of a service failure. Notification providers need to track only those notifications sent between checkpoints and must resend them if the catalog is restored or reset.
            


                If a catalog restore occurs, the search service rolls back the catalog to the last saved checkpoint and updates the <i>guidCheckPointSignature</i>. In this situation, notification providers must resend all notifications accumulated since the most recent saved checkpoint, as identified by the <i>dwLastCheckPointNumber</i> parameter.
            


                If a catalog reset occurs, the search service resets the entire catalog and updates the <i>guidCatalogResetSignature</i>. The notification provider must resend its entire crawl scope.
            




## -see-also




<a href="https://msdn.microsoft.com/5837ccf6-1156-44a5-9135-3e3b47244f9d">ISearchNotifyInlineSite</a>



<a href="https://msdn.microsoft.com/817550e2-a256-48d5-9fa6-1ea04f8b8589">Notifying the Index of Changes</a>
 

 


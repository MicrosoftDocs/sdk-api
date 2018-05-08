---
UID: NF:searchapi.ISearchNotifyInlineSite.OnCatalogStatusChange
title: ISearchNotifyInlineSite::OnCatalogStatusChange
author: windows-driver-content
description: Called by the search service to notify a client when the status of the catalog changes.
old-location: search\_search_ISearchNotifyInlineSite_OnCatalogStatusChange.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchnotifyinlinesite\oncatalogstatuschange.htm
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: ISearchNotifyInlineSite interface [search],OnCatalogStatusChange method, ISearchNotifyInlineSite.OnCatalogStatusChange, ISearchNotifyInlineSite::OnCatalogStatusChange, OnCatalogStatusChange, OnCatalogStatusChange method [search], OnCatalogStatusChange method [search],ISearchNotifyInlineSite interface, _search_ISearchNotifyInlineSite_OnCatalogStatusChange, search._search_ISearchNotifyInlineSite_OnCatalogStatusChange, searchapi/ISearchNotifyInlineSite::OnCatalogStatusChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchntfyinlinesite.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchNotifyInlineSite.OnCatalogStatusChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 


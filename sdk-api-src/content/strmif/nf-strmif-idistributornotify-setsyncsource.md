---
UID: NF:strmif.IDistributorNotify.SetSyncSource
title: IDistributorNotify::SetSyncSource (strmif.h)
author: windows-sdk-content
description: The SetSyncSource method is called when a new clock is registered.
old-location: dshow\idistributornotify_setsyncsource.htm
tech.root: DirectShow
ms.assetid: 671af56f-a333-441e-9a97-04226b1c3225
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDistributorNotify interface [DirectShow],SetSyncSource method, IDistributorNotify.SetSyncSource, IDistributorNotify::SetSyncSource, IDistributorNotifySetSyncSource, SetSyncSource, SetSyncSource method [DirectShow], SetSyncSource method [DirectShow],IDistributorNotify interface, dshow.idistributornotify_setsyncsource, strmif/IDistributorNotify::SetSyncSource
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDistributorNotify.SetSyncSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDistributorNotify::SetSyncSource


## -description



The <code>SetSyncSource</code> method is called when a new clock is registered.




## -parameters




### -param pClock [in]

Pointer to the new clock's <a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock</a> interface.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method is called before the filters are notified. Make sure to use <b>AddRef</b> on the <i>pClock</i> parameter if the plug-in distributor intends to hold it beyond this method call.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c7c9ee95-9d68-45c5-a3ca-8d6071782851">IDistributorNotify Interface</a>
 

 


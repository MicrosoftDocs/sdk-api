---
UID: NF:strmif.IDistributorNotify.NotifyGraphChange
title: IDistributorNotify::NotifyGraphChange
author: windows-sdk-content
description: The NotifyGraphChange method is called when the set of filters in the filter graph changes or any pin connections change.
old-location: dshow\idistributornotify_notifygraphchange.htm
tech.root: DirectShow
ms.assetid: 5f77f674-643a-450a-9589-16866d6cf680
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDistributorNotify interface [DirectShow],NotifyGraphChange method, IDistributorNotify.NotifyGraphChange, IDistributorNotify::NotifyGraphChange, IDistributorNotifyNotifyGraphChange, NotifyGraphChange, NotifyGraphChange method [DirectShow], NotifyGraphChange method [DirectShow],IDistributorNotify interface, dshow.idistributornotify_notifygraphchange, strmif/IDistributorNotify::NotifyGraphChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDistributorNotify.NotifyGraphChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IDistributorNotify.NotifyGraphChange
: 
---

# IDistributorNotify::NotifyGraphChange


## -description



The <code>NotifyGraphChange</code> method is called when the set of filters in the filter graph changes or any pin connections change.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method is called whenever the <a href="https://msdn.microsoft.com/8f837917-015f-427f-b234-b0ccbcf943eb">IFilterGraph::AddFilter</a>, <a href="https://msdn.microsoft.com/ec681340-0fb9-4eba-8211-d5fa07fb076b">IFilterGraph::RemoveFilter</a>, or <a href="https://msdn.microsoft.com/fb17bd98-dd6b-4fad-9b56-9cab10725b28">IFilterGraph::ConnectDirect</a> method is called or a method is called that will lead to one of these being called (such as <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a>).

Make sure you call <b>Release</b> on any held filters that have been removed at this point. For performance reasons, PIDs might choose not to rescan the filters until the PIDs actually need the interfaces, because there might be several separate notifications sent. However, it is important to release any cached interfaces immediately.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c7c9ee95-9d68-45c5-a3ca-8d6071782851">IDistributorNotify Interface</a>
 

 


---
UID: NF:subscriptionservices.IWMPSubscriptionService.startBackgroundProcessing
title: IWMPSubscriptionService::startBackgroundProcessing (subscriptionservices.h)
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpsubscriptionservice_startbackgroundprocessing.htm
tech.root: WMP
ms.assetid: a3bdb4b1-8479-484f-92db-2b73a0c40bfb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPSubscriptionService interface [Windows Media Player],startBackgroundProcessing method, IWMPSubscriptionService.startBackgroundProcessing, IWMPSubscriptionService::startBackgroundProcessing, IWMPSubscriptionServicestartBackgroundProcessing, startBackgroundProcessing, startBackgroundProcessing method [Windows Media Player], startBackgroundProcessing method [Windows Media Player],IWMPSubscriptionService interface, subscriptionservices/IWMPSubscriptionService::startBackgroundProcessing, wmp.iwmpsubscriptionservice_startbackgroundprocessing
ms.topic: method
f1_keywords: 
 - "subscriptionservices/IWMPSubscriptionService.startBackgroundProcessing"
dev_langs:
 - c++
req.header: subscriptionservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - subscriptionservices.h
api_name:
 - IWMPSubscriptionService.startBackgroundProcessing
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSubscriptionService::startBackgroundProcessing


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>startBackgroundProcessing</b> method is implemented by the online store to initiate background processing tasks.




## -parameters




### -param hwnd [in]

A handle to a window in which the plug-in can display a user interface.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Your code should not perform lengthy operations synchronously when Windows Media Player calls this method. Instead, you must perform time-consuming tasks on a separate worker thread.

Windows Media Player calls <b>startBackgroundProcessing</b> during idle time after the user selects the online store. This is useful for the online store to acquire play count data or renew expired licenses.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice">IWMPSubscriptionService Interface</a>
 

 


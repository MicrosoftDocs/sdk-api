---
UID: NF:mbnapi.IMbnInterfaceEvents.OnPreferredProvidersChange
title: IMbnInterfaceEvents::OnPreferredProvidersChange (mbnapi.h)
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate a change in a device's preferred provider list.
old-location: mbn\imbninterfaceevents_onpreferredproviderschange.htm
tech.root: mbn
ms.assetid: ccede3de-4dfd-469f-afb4-d1424c56c7bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnPreferredProvidersChange method, IMbnInterfaceEvents.OnPreferredProvidersChange, IMbnInterfaceEvents::OnPreferredProvidersChange, OnPreferredProvidersChange, OnPreferredProvidersChange method [Microsoft Broadband Networks], OnPreferredProvidersChange method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_onpreferredproviderschange, mbnapi/IMbnInterfaceEvents::OnPreferredProvidersChange
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnInterfaceEvents.OnPreferredProvidersChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnInterfaceEvents::OnPreferredProvidersChange


## -description


This notification method is called by the Mobile Broadband service to indicate a change in a device's preferred provider list.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> that represents the Mobile Broadband device whose preferred provider list has changed.


## -returns



This method must return <b>S_OK</b>.




## -remarks



In some cases, a device's preferred provider list can be updated by the network by SMS or OTA (over The air) update. The Mobile Broadband service will call this method to notify the application about any change in the preferred provider list. The application can call the <a href="https://msdn.microsoft.com/cbd37f0a-4245-415d-bd74-501aa4c7ade7">GetPreferredProviders</a> method of the passed <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> to get the updated list of preferred providers.


If there is a change in the preferred provider list because of a call to the <a href="https://msdn.microsoft.com/2ea95b4a-07d9-40d6-bb82-091b49c965c4">SetPreferredProviders</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>, then this notification will not be called. 













## -see-also




<a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>
 

 


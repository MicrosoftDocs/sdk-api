---
UID: NF:mbnapi.IMbnInterfaceEvents.OnHomeProviderAvailable
title: IMbnInterfaceEvents::OnHomeProviderAvailable (mbnapi.h)
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate that home provider information for the device is available.
old-location: mbn\imbninterfaceevents_onhomeprovideravailable.htm
tech.root: mbn
ms.assetid: 4da50033-d55c-4878-b05c-cbc43c156da0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnHomeProviderAvailable method, IMbnInterfaceEvents.OnHomeProviderAvailable, IMbnInterfaceEvents::OnHomeProviderAvailable, OnHomeProviderAvailable, OnHomeProviderAvailable method [Microsoft Broadband Networks], OnHomeProviderAvailable method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_onhomeprovideravailable, mbnapi/IMbnInterfaceEvents::OnHomeProviderAvailable
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnInterfaceEvents.OnHomeProviderAvailable"
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
 - IMbnInterfaceEvents.OnHomeProviderAvailable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnInterfaceEvents::OnHomeProviderAvailable


## -description


This notification method is called by the Mobile Broadband service to indicate that home provider information for the device is available.


## -parameters




### -param newInterface [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents the device whose home provider information has become available.


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can call the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-gethomeprovider">GetHomeProvider</a> method of  the passed <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> to get the available home provider information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>
 

 


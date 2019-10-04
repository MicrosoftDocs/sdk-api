---
UID: NF:mbnapi.IMbnConnectionContextEvents.OnProvisionedContextListChange
title: IMbnConnectionContextEvents::OnProvisionedContextListChange (mbnapi.h)
author: windows-sdk-content
description: Notification method called by the Mobile Broadband service to indicate that a provisioned context stored in the device is available or updated.
old-location: mbn\imbnconnectioncontextevents_onprovisionedcontextlistchange.htm
tech.root: mbn
ms.assetid: 3c8fa150-7c36-4ad8-ada8-2b17693671d9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnConnectionContextEvents interface [Microsoft Broadband Networks],OnProvisionedContextListChange method, IMbnConnectionContextEvents.OnProvisionedContextListChange, IMbnConnectionContextEvents::OnProvisionedContextListChange, OnProvisionedContextListChange, OnProvisionedContextListChange method [Microsoft Broadband Networks], OnProvisionedContextListChange method [Microsoft Broadband Networks],IMbnConnectionContextEvents interface, mbn.imbnconnectioncontextevents_onprovisionedcontextlistchange, mbnapi/IMbnConnectionContextEvents::OnProvisionedContextListChange
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnConnectionContextEvents.OnProvisionedContextListChange"
dev_langs:
 - c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IMbnConnectionContextEvents.OnProvisionedContextListChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnConnectionContextEvents::OnProvisionedContextListChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method called by the Mobile Broadband service to indicate that a provisioned context stored in the device is available or updated.


## -parameters




### -param newInterface [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontext">IMbnConnectionContext</a> interface that represents the device for which the context is available or updated.


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can use the passed <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontext">IMbnConnectionContext</a> interface to get the list of provisioned contexts for the device.  

<b>OnProvisionedContextListChange</b> is not called as the result of an update to an existing provisioned context from an application call of the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectioncontext-setprovisionedcontext">SetProvisionedContext</a> method of <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontext">IMbnConnectionContext</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontextevents">IMbnConnectionContextEvents</a>
 

 


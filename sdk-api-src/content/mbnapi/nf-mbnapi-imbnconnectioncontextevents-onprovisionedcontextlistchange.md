---
UID: NF:mbnapi.IMbnConnectionContextEvents.OnProvisionedContextListChange
title: IMbnConnectionContextEvents::OnProvisionedContextListChange
author: windows-sdk-content
description: Notification method called by the Mobile Broadband service to indicate that a provisioned context stored in the device is available or updated.
old-location: mbn\imbnconnectioncontextevents_onprovisionedcontextlistchange.htm
old-project: mbn
ms.assetid: 3c8fa150-7c36-4ad8-ada8-2b17693671d9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMbnConnectionContextEvents interface [Microsoft Broadband Networks],OnProvisionedContextListChange method, IMbnConnectionContextEvents.OnProvisionedContextListChange, IMbnConnectionContextEvents::OnProvisionedContextListChange, OnProvisionedContextListChange, OnProvisionedContextListChange method [Microsoft Broadband Networks], OnProvisionedContextListChange method [Microsoft Broadband Networks],IMbnConnectionContextEvents interface, mbn.imbnconnectioncontextevents_onprovisionedcontextlistchange, mbnapi/IMbnConnectionContextEvents::OnProvisionedContextListChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionContextEvents.OnProvisionedContextListChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionContextEvents::OnProvisionedContextListChange


## -description


Notification method called by the Mobile Broadband service to indicate that a provisioned context stored in the device is available or updated.


## -parameters




### -param newInterface [in]

An <a href="https://msdn.microsoft.com/a9bc52dc-47f9-4b20-b98d-0287464a89e5">IMbnConnectionContext</a> interface that represents the device for which the context is available or updated.


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can use the passed <a href="https://msdn.microsoft.com/a9bc52dc-47f9-4b20-b98d-0287464a89e5">IMbnConnectionContext</a> interface to get the list of provisioned contexts for the device.  

<b>OnProvisionedContextListChange</b> is not called as the result of an update to an existing provisioned context from an application call of the <a href="https://msdn.microsoft.com/738a3037-01a9-465a-a67d-979a29968b68">SetProvisionedContext</a> method of <a href="https://msdn.microsoft.com/a9bc52dc-47f9-4b20-b98d-0287464a89e5">IMbnConnectionContext</a>.




## -see-also




<a href="https://msdn.microsoft.com/1f73260b-04db-410a-ade0-a835805b2b0a">IMbnConnectionContextEvents</a>
 

 


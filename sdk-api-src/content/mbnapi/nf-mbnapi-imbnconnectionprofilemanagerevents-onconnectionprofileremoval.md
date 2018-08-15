---
UID: NF:mbnapi.IMbnConnectionProfileManagerEvents.OnConnectionProfileRemoval
title: IMbnConnectionProfileManagerEvents::OnConnectionProfileRemoval
author: windows-sdk-content
description: Notification method that indicates a connection profile has been removed from the system.
old-location: mbn\imbnconnectionprofilemanagerevents_onconnectionprofileremoval.htm
old-project: mbn
ms.assetid: 30b8c7fb-5a48-4025-aa94-18f17e7c8d19
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks],OnConnectionProfileRemoval method, IMbnConnectionProfileManagerEvents.OnConnectionProfileRemoval, IMbnConnectionProfileManagerEvents::OnConnectionProfileRemoval, OnConnectionProfileRemoval, OnConnectionProfileRemoval method [Microsoft Broadband Networks], OnConnectionProfileRemoval method [Microsoft Broadband Networks],IMbnConnectionProfileManagerEvents interface, mbn.imbnconnectionprofilemanagerevents_onconnectionprofileremoval, mbnapi/IMbnConnectionProfileManagerEvents::OnConnectionProfileRemoval
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
 - IMbnConnectionProfileManagerEvents.OnConnectionProfileRemoval
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionProfileManagerEvents::OnConnectionProfileRemoval


## -description


Notification method that indicates a connection profile has been removed from the system.


## -parameters




### -param oldConnectionProfile [in]

An <a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a> interface that represents a connection profile that has been removed.


## -returns



This method must return <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/08ec0bff-898f-4a54-b711-ceae80e7329d">IMbnConnectionProfileManagerEvents</a>
 

 


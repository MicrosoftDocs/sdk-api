---
UID: NF:mbnapi.IMbnConnectionProfileManagerEvents.OnConnectionProfileRemoval
title: IMbnConnectionProfileManagerEvents::OnConnectionProfileRemoval (mbnapi.h)
author: windows-sdk-content
description: Notification method that indicates a connection profile has been removed from the system.
old-location: mbn\imbnconnectionprofilemanagerevents_onconnectionprofileremoval.htm
tech.root: mbn
ms.assetid: 30b8c7fb-5a48-4025-aa94-18f17e7c8d19
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks],OnConnectionProfileRemoval method, IMbnConnectionProfileManagerEvents.OnConnectionProfileRemoval, IMbnConnectionProfileManagerEvents::OnConnectionProfileRemoval, OnConnectionProfileRemoval, OnConnectionProfileRemoval method [Microsoft Broadband Networks], OnConnectionProfileRemoval method [Microsoft Broadband Networks],IMbnConnectionProfileManagerEvents interface, mbn.imbnconnectionprofilemanagerevents_onconnectionprofileremoval, mbnapi/IMbnConnectionProfileManagerEvents::OnConnectionProfileRemoval
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnConnectionProfileManagerEvents.OnConnectionProfileRemoval"
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
 - IMbnConnectionProfileManagerEvents.OnConnectionProfileRemoval
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnConnectionProfileManagerEvents::OnConnectionProfileRemoval


## -description


Notification method that indicates a connection profile has been removed from the system.


## -parameters




### -param oldConnectionProfile [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a> interface that represents a connection profile that has been removed.


## -returns



This method must return <b>S_OK</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanagerevents">IMbnConnectionProfileManagerEvents</a>
 

 


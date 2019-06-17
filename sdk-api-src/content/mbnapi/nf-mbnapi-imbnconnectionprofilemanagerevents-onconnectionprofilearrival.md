---
UID: NF:mbnapi.IMbnConnectionProfileManagerEvents.OnConnectionProfileArrival
title: IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival (mbnapi.h)
author: windows-sdk-content
description: Notification method that indicates a new connection profile has been added to the system.
old-location: mbn\imbnconnectionprofilemanagerevents_onconnectionprofilearrival.htm
tech.root: mbn
ms.assetid: 94338c8c-2a89-412f-811e-5c50ecd9be70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks],OnConnectionProfileArrival method, IMbnConnectionProfileManagerEvents.OnConnectionProfileArrival, IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival, OnConnectionProfileArrival, OnConnectionProfileArrival method [Microsoft Broadband Networks], OnConnectionProfileArrival method [Microsoft Broadband Networks],IMbnConnectionProfileManagerEvents interface, mbn.imbnconnectionprofilemanagerevents_onconnectionprofilearrival, mbnapi/IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival
ms.topic: method
f1_keywords: ["mbnapi/IMbnConnectionProfileManagerEvents.OnConnectionProfileArrival"]
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
 - IMbnConnectionProfileManagerEvents.OnConnectionProfileArrival
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival


## -description


Notification method that indicates a new connection profile has been added to the system.


## -parameters




### -param newConnectionProfile [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a> interface that represents a connection profile that has been added.


## -returns



This method must return <b>S_OK</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanagerevents">IMbnConnectionProfileManagerEvents</a>
 

 


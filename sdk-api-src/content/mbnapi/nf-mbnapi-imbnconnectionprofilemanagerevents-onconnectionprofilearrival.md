---
UID: NF:mbnapi.IMbnConnectionProfileManagerEvents.OnConnectionProfileArrival
title: IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival (mbnapi.h)
author: windows-sdk-content
description: Notification method that indicates a new connection profile has been added to the system.
old-location: mbn\imbnconnectionprofilemanagerevents_onconnectionprofilearrival.htm
tech.root: mbn
ms.assetid: 94338c8c-2a89-412f-811e-5c50ecd9be70
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMbnConnectionProfileManagerEvents interface [Microsoft Broadband Networks],OnConnectionProfileArrival method, IMbnConnectionProfileManagerEvents.OnConnectionProfileArrival, IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival, OnConnectionProfileArrival, OnConnectionProfileArrival method [Microsoft Broadband Networks], OnConnectionProfileArrival method [Microsoft Broadband Networks],IMbnConnectionProfileManagerEvents interface, mbn.imbnconnectionprofilemanagerevents_onconnectionprofilearrival, mbnapi/IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival
ms.topic: method
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
---

# IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival


## -description


Notification method that indicates a new connection profile has been added to the system.


## -parameters




### -param newConnectionProfile [in]

An <a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a> interface that represents a connection profile that has been added.


## -returns



This method must return <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/08ec0bff-898f-4a54-b711-ceae80e7329d">IMbnConnectionProfileManagerEvents</a>
 

 


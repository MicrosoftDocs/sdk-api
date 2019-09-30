---
UID: NF:mbnapi.IMbnInterfaceManagerEvents.OnInterfaceRemoval
title: IMbnInterfaceManagerEvents::OnInterfaceRemoval (mbnapi.h)
author: windows-sdk-content
description: Notification method that signals that a device has been removed from the system.
old-location: mbn\imbninterfacemanagerevents_oninterfaceremoval.htm
tech.root: mbn
ms.assetid: d7c96d35-20e1-46e2-82db-4b1fc03cdd22
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceManagerEvents interface [Microsoft Broadband Networks],OnInterfaceRemoval method, IMbnInterfaceManagerEvents.OnInterfaceRemoval, IMbnInterfaceManagerEvents::OnInterfaceRemoval, OnInterfaceRemoval, OnInterfaceRemoval method [Microsoft Broadband Networks], OnInterfaceRemoval method [Microsoft Broadband Networks],IMbnInterfaceManagerEvents interface, mbn.imbninterfacemanagerevents_oninterfaceremoval, mbnapi/IMbnInterfaceManagerEvents::OnInterfaceRemoval
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnInterfaceManagerEvents.OnInterfaceRemoval"
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
 - IMbnInterfaceManagerEvents.OnInterfaceRemoval
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnInterfaceManagerEvents::OnInterfaceRemoval


## -description


Notification method that signals that a device has been removed from the system.


## -parameters




### -param oldInterface [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents the device that was removed.


## -returns



This method must return <b>S_OK</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanagerevents">IMbnInterfaceManagerEvents</a>
 

 


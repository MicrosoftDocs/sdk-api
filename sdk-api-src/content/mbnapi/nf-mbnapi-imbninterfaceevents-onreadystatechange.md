---
UID: NF:mbnapi.IMbnInterfaceEvents.OnReadyStateChange
title: IMbnInterfaceEvents::OnReadyStateChange (mbnapi.h)
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate a change in an interface's ready state.
old-location: mbn\imbninterfaceevents_onreadystatechange.htm
tech.root: mbn
ms.assetid: eb4364b8-cbbf-44c7-ae13-66950ce614e9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnReadyStateChange method, IMbnInterfaceEvents.OnReadyStateChange, IMbnInterfaceEvents::OnReadyStateChange, OnReadyStateChange, OnReadyStateChange method [Microsoft Broadband Networks], OnReadyStateChange method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_onreadystatechange, mbnapi/IMbnInterfaceEvents::OnReadyStateChange
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnInterfaceEvents.OnReadyStateChange"
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
 - IMbnInterfaceEvents.OnReadyStateChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnInterfaceEvents::OnReadyStateChange


## -description


This notification method is called by the Mobile Broadband service to indicate a change in an interface's ready state.


## -parameters




### -param newInterface [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents the Mobile Broadband device whose ready state has changed.


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can call the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getreadystate">GetReadyState</a> method of the passed <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> to get latest ready state of the device. For a list of ready states, see  <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/ne-mbnapi-mbn_ready_state">MBN_READY_STATE</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>
 

 


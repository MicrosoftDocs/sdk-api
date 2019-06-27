---
UID: NF:mbnapi.IMbnPinManagerEvents.OnPinListAvailable
title: IMbnPinManagerEvents::OnPinListAvailable (mbnapi.h)
author: windows-sdk-content
description: Notification method called by the Mobile Broadband service to indicate that the list of device PINs is available.
old-location: mbn\imbnpinmanagerevents_onpinlistavailable.htm
tech.root: mbn
ms.assetid: 37347dd8-07c2-4521-a5f0-a51053634704
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnPinManagerEvents interface [Microsoft Broadband Networks],OnPinListAvailable method, IMbnPinManagerEvents.OnPinListAvailable, IMbnPinManagerEvents::OnPinListAvailable, OnPinListAvailable, OnPinListAvailable method [Microsoft Broadband Networks], OnPinListAvailable method [Microsoft Broadband Networks],IMbnPinManagerEvents interface, mbn.imbnpinmanagerevents_onpinlistavailable, mbnapi/IMbnPinManagerEvents::OnPinListAvailable
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnPinManagerEvents.OnPinListAvailable"
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
 - IMbnPinManagerEvents.OnPinListAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnPinManagerEvents::OnPinListAvailable


## -description


Notification method called by the Mobile Broadband service to indicate that the list of device PINs is available.


## -parameters




### -param pinManager [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> interface that represents the Mobile Broadband device for which the PIN list is available.


## -returns



This method must return <b>S_OK</b>.




## -remarks



This method is called by the Mobile Broadband service to notify an application when the list of supported PIN types is available or if a PIN list retrieval operation resulted in an error. The calling application can issue the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinlist">GetPinList</a> method of the passed <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> to get the available list of supported PINs or error code returned in the operation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanagerevents">IMbnPinManagerEvents</a>
 

 


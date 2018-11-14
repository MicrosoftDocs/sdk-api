---
UID: NF:mbnapi.IMbnPinManagerEvents.OnPinListAvailable
title: IMbnPinManagerEvents::OnPinListAvailable
author: windows-sdk-content
description: Notification method called by the Mobile Broadband service to indicate that the list of device PINs is available.
old-location: mbn\imbnpinmanagerevents_onpinlistavailable.htm
tech.root: mbn
ms.assetid: 37347dd8-07c2-4521-a5f0-a51053634704
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMbnPinManagerEvents interface [Microsoft Broadband Networks],OnPinListAvailable method, IMbnPinManagerEvents.OnPinListAvailable, IMbnPinManagerEvents::OnPinListAvailable, OnPinListAvailable, OnPinListAvailable method [Microsoft Broadband Networks], OnPinListAvailable method [Microsoft Broadband Networks],IMbnPinManagerEvents interface, mbn.imbnpinmanagerevents_onpinlistavailable, mbnapi/IMbnPinManagerEvents::OnPinListAvailable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
- apiref
: 
- COM
: 
- mbnapi.h
: 
- IMbnPinManagerEvents.OnPinListAvailable
: 
---

# IMbnPinManagerEvents::OnPinListAvailable


## -description


Notification method called by the Mobile Broadband service to indicate that the list of device PINs is available.


## -parameters




### -param pinManager [in]

Pointer to an <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a> interface that represents the Mobile Broadband device for which the PIN list is available.


## -returns



This method must return <b>S_OK</b>.




## -remarks



This method is called by the Mobile Broadband service to notify an application when the list of supported PIN types is available or if a PIN list retrieval operation resulted in an error. The calling application can issue the <a href="https://msdn.microsoft.com/732906dd-7d1e-49a1-a3cc-60075eed9c7c">GetPinList</a> method of the passed <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a> to get the available list of supported PINs or error code returned in the operation.




## -see-also




<a href="https://msdn.microsoft.com/2942bd4d-5bdb-45eb-a008-352bf44eec80">IMbnPinManagerEvents</a>
 

 


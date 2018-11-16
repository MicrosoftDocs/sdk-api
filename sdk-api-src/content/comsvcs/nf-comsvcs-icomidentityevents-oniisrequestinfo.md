---
UID: NF:comsvcs.IComIdentityEvents.OnIISRequestInfo
title: IComIdentityEvents::OnIISRequestInfo
author: windows-sdk-content
description: Generated when an activity is part of an ASP page.
old-location: cos\icomidentityevents_oniisrequestinfo.htm
tech.root: cossdk
ms.assetid: 88beaef9-d042-4836-8223-6063c87ba06a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IComIdentityEvents interface [COM+],OnIISRequestInfo method, IComIdentityEvents.OnIISRequestInfo, IComIdentityEvents::OnIISRequestInfo, OnIISRequestInfo, OnIISRequestInfo method [COM+], OnIISRequestInfo method [COM+],IComIdentityEvents interface, _dtc_IComIdentityEvents_OnIISRequestInfo, comsvcs/IComIdentityEvents::OnIISRequestInfo, cos.icomidentityevents_oniisrequestinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ComSvcs.h
api_name:
 - IComIdentityEvents.OnIISRequestInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IComIdentityEvents.OnIISRequestInfo
: 
---

# IComIdentityEvents::OnIISRequestInfo


## -description


Generated when an activity is part of an ASP page.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param ObjId [in]

The unique identifier for this object.


### -param pszClientIP [in]

The Internet Protocol (IP) address of the IIS client.


### -param pszServerIP [in]

The IP address of the IIS server.


### -param pszURL [in]

The URL on IIS server generating object reference.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/f064a5cd-c84d-4b80-96fc-1036af333901">IComIdentityEvents</a>
 

 


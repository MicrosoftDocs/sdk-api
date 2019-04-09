---
UID: NF:wuapi.IUpdateServiceManager2.QueryServiceRegistration
title: IUpdateServiceManager2::QueryServiceRegistration (wuapi.h)
author: windows-sdk-content
description: Returns a pointer to an IUpdateServiceRegistration interface.
old-location: wua\iupdateservicemanager2_queryserviceregistration_methods.htm
tech.root: Wua_Sdk
ms.assetid: d8fd077f-f4a9-4db0-8a47-14241bc574fb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUpdateServiceManager2 interface [Windows Update Agent],QueryServiceRegistration method, IUpdateServiceManager2.QueryServiceRegistration, IUpdateServiceManager2::QueryServiceRegistration, QueryServiceRegistration, QueryServiceRegistration method [Windows Update Agent], QueryServiceRegistration method [Windows Update Agent],IUpdateServiceManager2 interface, wua.iupdateservicemanager2_queryserviceregistration_methods, wuapi/IUpdateServiceManager2::QueryServiceRegistration
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateServiceManager2.QueryServiceRegistration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateServiceManager2::QueryServiceRegistration


## -description


Returns a pointer to an <a href="https://msdn.microsoft.com/729664f2-5f75-4e73-9ccc-150b2e201f66">IUpdateServiceRegistration</a> interface.


## -parameters




### -param serviceID [in]

An identifier for the service to be registered.


### -param retval [out]

A pointer to an <a href="https://msdn.microsoft.com/729664f2-5f75-4e73-9ccc-150b2e201f66">IUpdateServiceRegistration</a> interface that represents an added service.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/26b75edc-eb43-4ee0-8040-da8b3252cf21">IUpdateServiceManager2</a>
 

 


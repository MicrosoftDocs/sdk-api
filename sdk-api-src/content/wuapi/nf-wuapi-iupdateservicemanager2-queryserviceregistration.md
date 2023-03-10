---
UID: NF:wuapi.IUpdateServiceManager2.QueryServiceRegistration
title: IUpdateServiceManager2::QueryServiceRegistration (wuapi.h)
description: Returns a pointer to an IUpdateServiceRegistration interface.
helpviewer_keywords: ["IUpdateServiceManager2 interface [Windows Update Agent]","QueryServiceRegistration method","IUpdateServiceManager2.QueryServiceRegistration","IUpdateServiceManager2::QueryServiceRegistration","QueryServiceRegistration","QueryServiceRegistration method [Windows Update Agent]","QueryServiceRegistration method [Windows Update Agent]","IUpdateServiceManager2 interface","wua.iupdateservicemanager2_queryserviceregistration_methods","wuapi/IUpdateServiceManager2::QueryServiceRegistration"]
old-location: wua\iupdateservicemanager2_queryserviceregistration_methods.htm
tech.root: wua
ms.assetid: d8fd077f-f4a9-4db0-8a47-14241bc574fb
ms.date: 12/05/2018
ms.keywords: IUpdateServiceManager2 interface [Windows Update Agent],QueryServiceRegistration method, IUpdateServiceManager2.QueryServiceRegistration, IUpdateServiceManager2::QueryServiceRegistration, QueryServiceRegistration, QueryServiceRegistration method [Windows Update Agent], QueryServiceRegistration method [Windows Update Agent],IUpdateServiceManager2 interface, wua.iupdateservicemanager2_queryserviceregistration_methods, wuapi/IUpdateServiceManager2::QueryServiceRegistration
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateServiceManager2::QueryServiceRegistration
 - wuapi/IUpdateServiceManager2::QueryServiceRegistration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateServiceManager2.QueryServiceRegistration
---

# IUpdateServiceManager2::QueryServiceRegistration


## -description

Returns a pointer to an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateserviceregistration">IUpdateServiceRegistration</a> interface.

## -parameters

### -param serviceID [in]

An identifier for the service to be registered.

### -param retval [out]

A pointer to an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateserviceregistration">IUpdateServiceRegistration</a> interface that represents an added service.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager2">IUpdateServiceManager2</a>
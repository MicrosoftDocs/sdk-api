---
UID: NN:wuapi.IUpdateServiceManager2
title: IUpdateServiceManager2 (wuapi.h)
description: Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates. (IUpdateServiceManager2)
helpviewer_keywords: ["IUpdateServiceManager2","IUpdateServiceManager2 interface [Windows Update Agent]","IUpdateServiceManager2 interface [Windows Update Agent]","described","wua.iupdateservicemanager2","wuapi/IUpdateServiceManager2"]
old-location: wua\iupdateservicemanager2.htm
tech.root: wua
ms.assetid: 26b75edc-eb43-4ee0-8040-da8b3252cf21
ms.date: 12/05/2018
ms.keywords: IUpdateServiceManager2, IUpdateServiceManager2 interface [Windows Update Agent], IUpdateServiceManager2 interface [Windows Update Agent],described, wua.iupdateservicemanager2, wuapi/IUpdateServiceManager2
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
 - IUpdateServiceManager2
 - wuapi/IUpdateServiceManager2
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
 - IUpdateServiceManager2
---

# IUpdateServiceManager2 interface


## -description

 Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates.

## -inheritance

The <b>IUpdateServiceManager2</b> interface inherits from <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>. <b>IUpdateServiceManager2</b> also has these types of members:

## -remarks

You can create an instance of this interface by using the UpdateServiceManager coclass. Use the Microsoft.Update.ServiceManager program identifier to create the object.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>

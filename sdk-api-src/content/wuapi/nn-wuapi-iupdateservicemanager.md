---
UID: NN:wuapi.IUpdateServiceManager
title: IUpdateServiceManager (wuapi.h)
description: Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates. (IUpdateServiceManager)
helpviewer_keywords: ["IUpdateServiceManager","IUpdateServiceManager interface [Windows Update Agent]","IUpdateServiceManager interface [Windows Update Agent]","described","wua.iupdateservicemanager","wuapi/IUpdateServiceManager"]
old-location: wua\iupdateservicemanager.htm
tech.root: wua
ms.assetid: 99b451b8-9831-475c-a4b0-7809f78d91b8
ms.date: 12/05/2018
ms.keywords: IUpdateServiceManager, IUpdateServiceManager interface [Windows Update Agent], IUpdateServiceManager interface [Windows Update Agent],described, wua.iupdateservicemanager, wuapi/IUpdateServiceManager
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
 - IUpdateServiceManager
 - wuapi/IUpdateServiceManager
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
 - IUpdateServiceManager
---

# IUpdateServiceManager interface


## -description

Adds or removes the registration of the update service with Windows Update Agent or Automatic Updates.

## -inheritance

The <b>IUpdateServiceManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdateServiceManager</b> also has these types of members:

## -remarks

You can create an instance of this interface by using the UpdateServiceManager coclass. Use the Microsoft.Update.ServiceManager program identifier to create the object.

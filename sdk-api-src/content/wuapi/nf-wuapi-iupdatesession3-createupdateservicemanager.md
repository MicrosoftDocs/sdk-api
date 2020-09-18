---
UID: NF:wuapi.IUpdateSession3.CreateUpdateServiceManager
title: IUpdateSession3::CreateUpdateServiceManager (wuapi.h)
description: Returns a pointer to an IUpdateServiceManager2 interface for the session.
helpviewer_keywords: ["CreateUpdateServiceManager","CreateUpdateServiceManager method [Windows Update Agent]","CreateUpdateServiceManager method [Windows Update Agent]","IUpdateSession3 interface","IUpdateSession3 interface [Windows Update Agent]","CreateUpdateServiceManager method","IUpdateSession3.CreateUpdateServiceManager","IUpdateSession3::CreateUpdateServiceManager","wua.iupdatesession3_createupdateservicemanager","wuapi/IUpdateSession3::CreateUpdateServiceManager"]
old-location: wua\iupdatesession3_createupdateservicemanager.htm
tech.root: wua
ms.assetid: 79d8f489-5375-48e2-a40d-d6f38f4843aa
ms.date: 12/05/2018
ms.keywords: CreateUpdateServiceManager, CreateUpdateServiceManager method [Windows Update Agent], CreateUpdateServiceManager method [Windows Update Agent],IUpdateSession3 interface, IUpdateSession3 interface [Windows Update Agent],CreateUpdateServiceManager method, IUpdateSession3.CreateUpdateServiceManager, IUpdateSession3::CreateUpdateServiceManager, wua.iupdatesession3_createupdateservicemanager, wuapi/IUpdateSession3::CreateUpdateServiceManager
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
 - IUpdateSession3::CreateUpdateServiceManager
 - wuapi/IUpdateSession3::CreateUpdateServiceManager
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
 - IUpdateSession3.CreateUpdateServiceManager
---

# IUpdateSession3::CreateUpdateServiceManager


## -description

Returns a pointer to an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager2">IUpdateServiceManager2</a> interface for the session.

## -parameters

### -param retval [out]

A pointer to an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager2">IUpdateServiceManager2</a> interface for the session.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession3">IUpdateSession3</a>
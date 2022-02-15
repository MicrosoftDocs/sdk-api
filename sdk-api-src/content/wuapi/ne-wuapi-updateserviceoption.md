---
UID: NE:wuapi.tagUpdateServiceOption
title: UpdateServiceOption (wuapi.h)
description: Defines the options that affect how the service registration for a scan package service is removed.
helpviewer_keywords: ["UpdateServiceOption","UpdateServiceOption enumeration [Windows Update Agent]","usoNonVolatileService","wua.updateserviceoption","wuapi/UpdateServiceOption","wuapi/usoNonVolatileService"]
old-location: wua\updateserviceoption.htm
tech.root: wua
ms.assetid: c03ee4e7-b8d4-46bb-bc57-20b35d779e07
ms.date: 12/05/2018
ms.keywords: UpdateServiceOption, UpdateServiceOption enumeration [Windows Update Agent], usoNonVolatileService, wua.updateserviceoption, wuapi/UpdateServiceOption, wuapi/usoNonVolatileService
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UpdateServiceOption
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUpdateServiceOption
 - wuapi/tagUpdateServiceOption
 - UpdateServiceOption
 - wuapi/UpdateServiceOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - UpdateServiceOption
---

# UpdateServiceOption enumeration


## -description

Defines the options that  affect how the service registration for a scan package service is removed.

## -enum-fields

### -field usoNonVolatileService:0x1

Indicates that you must call the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-removeservice">IUpdateServiceManager::RemoveService</a> method to remove the service registration. 

Failure to call the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-removeservice">RemoveService</a> method before releasing the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservice">IUpdateService</a> interface causes a resource leak.

## -remarks

If you do not specify <b>usoNonVolatileService</b>, the service registration is automatically removed when you release the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservice">IUpdateService</a> interface.

The <b>UpdateServiceOption</b> enumeration  may require that you update Windows Update Agent (WUA). For more information, see <a href="/windows/desktop/Wua_Sdk/updating-the-windows-update-agent">Updating Windows Update Agent</a>.

## -see-also

<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice">IUpdateServiceManager::AddScanPackageService</a>

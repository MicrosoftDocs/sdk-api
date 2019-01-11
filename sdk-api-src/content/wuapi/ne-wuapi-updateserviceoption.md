---
UID: NE:wuapi.tagUpdateServiceOption
title: UpdateServiceOption
author: windows-sdk-content
description: Defines the options that affect how the service registration for a scan package service is removed.
old-location: wua\updateserviceoption.htm
tech.root: Wua_Sdk
ms.assetid: c03ee4e7-b8d4-46bb-bc57-20b35d779e07
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UpdateServiceOption, UpdateServiceOption enumeration [Windows Update Agent], usoNonVolatileService, wua.updateserviceoption, wuapi/UpdateServiceOption, wuapi/usoNonVolatileService
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - UpdateServiceOption
product: Windows
targetos: Windows
req.typenames: UpdateServiceOption
req.redist: 
---

# UpdateServiceOption enumeration


## -description


Defines the options that  affect how the service registration for a scan package service is removed.


## -enum-fields




### -field usoNonVolatileService

Indicates that you must call the <a href="https://msdn.microsoft.com/fedd0979-1cc1-40c7-93d1-ade2f069ee76">IUpdateServiceManager::RemoveService</a> method to remove the service registration. 

Failure to call the <a href="https://msdn.microsoft.com/fedd0979-1cc1-40c7-93d1-ade2f069ee76">RemoveService</a> method before releasing the <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> interface causes a resource leak.


## -remarks



If you do not specify <b>usoNonVolatileService</b>, the service registration is automatically removed when you release the <a href="https://msdn.microsoft.com/2f237cd3-668b-4b1b-b98b-4cfc40f5889e">IUpdateService</a> interface.

The <b>UpdateServiceOption</b> enumeration  may require that you update Windows Update Agent (WUA). For more information, see <a href="https://msdn.microsoft.com/829112ab-b240-4cc4-8053-18b484934886">Updating Windows Update Agent</a>.




## -see-also




<a href="https://msdn.microsoft.com/5b0677bb-9f19-4bb4-9942-8ca3da18b29a">IUpdateServiceManager::AddScanPackageService</a>
 

 


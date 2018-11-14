---
UID: NF:comadmin.ICOMAdminCatalog.RefreshComponents
title: ICOMAdminCatalog::RefreshComponents
author: windows-sdk-content
description: Updates component registration information from the registry.
old-location: cos\icomadmincatalog_refreshcomponents.htm
tech.root: cossdk
ms.assetid: 50528312-60e1-4648-b0e5-709a6b49737e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICOMAdminCatalog interface [COM+],RefreshComponents method, ICOMAdminCatalog.RefreshComponents, ICOMAdminCatalog::RefreshComponents, RefreshComponents, RefreshComponents method [COM+], RefreshComponents method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_RefreshComponents, comadmin/ICOMAdminCatalog::RefreshComponents, cos.icomadmincatalog_refreshcomponents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.RefreshComponents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comadmin.h
: 
- ICOMAdminCatalog.RefreshComponents
: 
---

# ICOMAdminCatalog::RefreshComponents


## -description


Updates component registration information from the registry.

You generally should not use <b>RefreshComponents</b>. The recommended way to update components in COM+ applications is to remove and reinstall the components using <a href="https://msdn.microsoft.com/en-us/library/ms681794(v=VS.85).aspx">ICOMAdminCatalog::InstallComponent</a> so that complete registration information is updated in the registry database.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The <b>RefreshComponents</b> method is called from within the Microsoft Visual Basic 6.0 development environment when you use the <b>Auto-refresh</b> or <b>Refresh all</b> components now features from the <b>Component Services</b> submenu of the <b>Add-Ins</b> menu.

To find mismatches, <b>RefreshComponents</b> compares CLSIDs and ProgIDs between the COM+ class registration database (RegDB) and the registry. This method updates components only when there is both a mismatch between CLSIDs and a match between corresponding ProgIDs.

Only CLSID information is updated to RegDB. No interface or method information is updated. Components that are refreshed using <b>RefreshComponents</b> cannot be configured or secured at the interface or method levels within COM+ applications.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee309561(v=VS.85).aspx">ICOMAdminCatalog</a>
 

 


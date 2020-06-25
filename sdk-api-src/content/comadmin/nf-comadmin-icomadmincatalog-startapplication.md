---
UID: NF:comadmin.ICOMAdminCatalog.StartApplication
title: ICOMAdminCatalog::StartApplication (comadmin.h)
description: Starts the specified COM+ server application. The application components are launched in a dedicated server process.
helpviewer_keywords: ["ICOMAdminCatalog interface [COM+]","StartApplication method","ICOMAdminCatalog.StartApplication","ICOMAdminCatalog::StartApplication","StartApplication","StartApplication method [COM+]","StartApplication method [COM+]","ICOMAdminCatalog interface","_cos_ICOMAdminCatalog_StartApplication","comadmin/ICOMAdminCatalog::StartApplication","cos.icomadmincatalog_startapplication"]
old-location: cos\icomadmincatalog_startapplication.htm
tech.root: cossdk
ms.assetid: 89423f39-7cbd-42dd-8d4a-6f312884e0bf
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog interface [COM+],StartApplication method, ICOMAdminCatalog.StartApplication, ICOMAdminCatalog::StartApplication, StartApplication, StartApplication method [COM+], StartApplication method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_StartApplication, comadmin/ICOMAdminCatalog::StartApplication, cos.icomadmincatalog_startapplication
f1_keywords:
- comadmin/ICOMAdminCatalog.StartApplication
dev_langs:
- c++
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
- ICOMAdminCatalog.StartApplication
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICOMAdminCatalog::StartApplication


## -description


Starts the specified COM+ server application. The application components are launched in a dedicated server process.


## -parameters




### -param bstrApplIdOrName [in]

The GUID or name of the application. If a GUID is used, it must be surrounded by braces.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>
 

 


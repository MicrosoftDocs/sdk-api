---
UID: NF:comadmin.ICOMAdminCatalog.ImportComponent
title: ICOMAdminCatalog::ImportComponent
author: windows-sdk-content
description: Imports a component already registered as an in-process server into a COM+ application.
old-location: cos\icomadmincatalog_importcomponent.htm
old-project: cossdk
ms.assetid: 0e29025d-60bc-4f95-a6f9-aa178769855c
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: ICOMAdminCatalog interface [COM+],ImportComponent method, ICOMAdminCatalog.ImportComponent, ICOMAdminCatalog::ImportComponent, ImportComponent, ImportComponent method [COM+], ImportComponent method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_ImportComponent, comadmin/ICOMAdminCatalog::ImportComponent, cos.icomadmincatalog_importcomponent
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.ImportComponent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog::ImportComponent


## -description


Imports a component already registered as an in-process server into a COM+ application.


## -parameters




### -param bstrApplIDOrName [in]

The GUID or name of the application.


### -param bstrCLSIDOrProgID [in]

The CLSID or ProgID for the component to import.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Generally, this method should not be used unless you want to restrict a component to local use only. Otherwise, use the <a href="https://msdn.microsoft.com/63af9aa4-a1f0-4277-bd36-8b4c64227b3f">InstallComponent</a> method instead of <b>ImportComponent</b>. <b>InstallComponent</b> fully registers the component in the COM+ class registration database (RegDB), whereas <b>ImportComponent</b> does not, resulting in an application with limited functionality.

<b>ImportComponent</b> does not bring any interface, method, or type library information for the component into the COM+ class registration database. This behavior restricts how the component can be configured. When you attempt to export a COM+ application that has an imported component to an application proxy, the proxy contains no interface or type library information for the component and marshaling for that component fails.




## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 


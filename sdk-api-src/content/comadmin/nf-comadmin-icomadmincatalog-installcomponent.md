---
UID: NF:comadmin.ICOMAdminCatalog.InstallComponent
title: ICOMAdminCatalog::InstallComponent (comadmin.h)
author: windows-sdk-content
description: Installs all components (COM classes) from a DLL file into a COM+ application and registers the components in the COM+ class registration database.
old-location: cos\icomadmincatalog_installcomponent.htm
tech.root: cossdk
ms.assetid: 63af9aa4-a1f0-4277-bd36-8b4c64227b3f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog interface [COM+],InstallComponent method, ICOMAdminCatalog.InstallComponent, ICOMAdminCatalog::InstallComponent, InstallComponent, InstallComponent method [COM+], InstallComponent method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_InstallComponent, comadmin/ICOMAdminCatalog::InstallComponent, cos.icomadmincatalog_installcomponent
ms.topic: method
f1_keywords: ["comadmin/ICOMAdminCatalog.InstallComponent"]
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
 - ICOMAdminCatalog.InstallComponent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICOMAdminCatalog::InstallComponent


## -description


Installs all components (COM classes) from a DLL file into a COM+ application and registers the components in the COM+ class registration database.


## -parameters




### -param bstrApplIDOrName [in]

The GUID or name of the application.


### -param bstrDLL [in]

The name of the DLL file containing the component to be installed.


### -param bstrTLB [in]

The name of the external type library file. If the type library file is embedded in the DLL, pass in an empty string for this parameter.


### -param bstrPSDLL [in]

The name of the proxy-stub DLL file. If there is no proxy-stub DLL associated with the component, pass in an empty string for this parameter.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



<b>InstallComponent</b> provides full registration of components in the COM+ class registration database (RegDB) as configured components, including interface, method, type library, and proxy-stub information necessary for marshaling. 

<b>InstallComponent</b> is the recommended way to install all components into COM+ applications instead of <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog-importcomponent">ICOMAdminCatalog::ImportComponent</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>
 

 


---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

<b>InstallComponent</b> is the recommended way to install all components into COM+ applications instead of <a href="https://msdn.microsoft.com/0e29025d-60bc-4f95-a6f9-aa178769855c">ICOMAdminCatalog::ImportComponent</a>. 




## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 


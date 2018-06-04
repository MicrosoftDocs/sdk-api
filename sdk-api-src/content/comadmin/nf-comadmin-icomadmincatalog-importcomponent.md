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
 

 


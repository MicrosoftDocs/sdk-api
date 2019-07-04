---
UID: NF:comsvcs.IComAppEvents.OnAppForceShutdown
title: IComAppEvents::OnAppForceShutdown (comsvcs.h)
author: windows-sdk-content
description: Generated when an application server is forced to shut down.
old-location: cos\icomappevents_onappforceshutdown.htm
tech.root: cossdk
ms.assetid: a7e845fc-be7f-484f-88b9-78206598b57d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComAppEvents interface [COM+],OnAppForceShutdown method, IComAppEvents.OnAppForceShutdown, IComAppEvents::OnAppForceShutdown, OnAppForceShutdown, OnAppForceShutdown method [COM+], OnAppForceShutdown method [COM+],IComAppEvents interface, _dtc_icomappevents_onappforceshutdown, comsvcs/IComAppEvents::OnAppForceShutdown, cos.icomappevents_onappforceshutdown
ms.topic: method
f1_keywords: 
 - "comsvcs/IComAppEvents.OnAppForceShutdown"
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - comsvcs.h
api_name:
 - IComAppEvents.OnAppForceShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComAppEvents::OnAppForceShutdown


## -description


Generated when an application server is forced to shut down. This is usually initiated by the user calling a catalog method, such as <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog-shutdownapplication">ICOMAdminCatalog::ShutdownApplication</a>, to shut down the server.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.


### -param guidApp [in]

The globally unique identifier (GUID) of the application.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomappevents">IComAppEvents</a>
 

 


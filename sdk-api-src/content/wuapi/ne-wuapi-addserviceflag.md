---
UID: NE:wuapi.tagAddServiceFlag
title: AddServiceFlag (wuapi.h)
author: windows-sdk-content
description: Defines the possible ways in which the IUpdateServiceManager2 interface can process service registration requests.
old-location: wua\addserviceflag.htm
tech.root: Wua_Sdk
ms.assetid: 1372a062-9f62-4b4d-8476-b6c7059a801a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddServiceFlag, AddServiceFlag enumeration [Windows Update Agent], asfAllowOnlineRegistration, asfAllowPendingRegistration, asfRegisterServiceWithAU, wua.addserviceflag, wuapi/AddServiceFlag, wuapi/asfAllowOnlineRegistration, wuapi/asfAllowPendingRegistration, wuapi/asfRegisterServiceWithAU
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
 - AddServiceFlag
product: Windows
targetos: Windows
req.typenames: AddServiceFlag
req.redist: 
ms.custom: 19H1
---

# AddServiceFlag enumeration


## -description


Defines the possible ways in which the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager2">IUpdateServiceManager2</a> interface can process service registration requests.


## -enum-fields




### -field asfAllowPendingRegistration

Allows the update agent to process the service registration at a later time, when it next performs an online scan for updates.


### -field asfAllowOnlineRegistration

Allows the update agent to process the service registration immediately if network connectivity is available.


### -field asfRegisterServiceWithAU

Registers the service with Automatic Updates when the service is added.


## -remarks



For info about how  <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager2-addservice2">IUpdateServiceManager2::AddService2</a> behaves when you specify different combinations of <b>AddServiceFlag</b> values in the <i>flags</i> parameter, see the Remarks section of <b>IUpdateServiceManager2::AddService2</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateservicemanager2-addservice2">IUpdateServiceManager2::AddService2</a>
 

 


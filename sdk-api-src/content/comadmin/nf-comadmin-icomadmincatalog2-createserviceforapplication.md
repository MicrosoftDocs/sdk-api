---
UID: NF:comadmin.ICOMAdminCatalog2.CreateServiceForApplication
title: ICOMAdminCatalog2::CreateServiceForApplication
author: windows-sdk-content
description: Configures a COM+ application to run as a Windows service.
old-location: cos\icomadmincatalog2_createserviceforapplication.htm
tech.root: cossdk
ms.assetid: 9ffc7366-c47a-487e-b40c-bdcea5dbf052
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateServiceForApplication, CreateServiceForApplication method [COM+], CreateServiceForApplication method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],CreateServiceForApplication method, ICOMAdminCatalog2.CreateServiceForApplication, ICOMAdminCatalog2::CreateServiceForApplication, _cos_icomadmincatalog2_CreateServiceForApplication, comadmin/ICOMAdminCatalog2::CreateServiceForApplication, cos.icomadmincatalog2_createserviceforapplication
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ICOMAdminCatalog2.CreateServiceForApplication
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
- ICOMAdminCatalog2.CreateServiceForApplication
: 
---

# ICOMAdminCatalog2::CreateServiceForApplication


## -description


Configures  a COM+ application to run as a Windows service.


## -parameters




### -param bstrApplicationIDOrName [in]

The application ID or name of the application.


### -param bstrServiceName [in]

 The service name of the application. This name is the internal name used by the service control manager (SCM), not the display name.


### -param bstrStartType [in]

When to start the service. The valid arguments are the options of the <i>dwStartType</i> parameter of the <a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function. The arguments must be in quotes. The following are the valid arguments: SERVICE_BOOT_START, SERVICE_SYSTEM_START, SERVICE_AUTO_START, SERVICE_DEMAND_START, and SERVICE_DISABLED.


### -param bstrErrorControl [in]

The severity of the error if this service fails to start during startup. The error determines the action taken by the startup program if failure occurs. The valid arguments are the options of the <i>dwErrorControl</i> parameter of the <a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function. The arguments must be in quotes. The following are the valid arguments: SERVICE_ERROR_IGNORE, SERVICE_ERROR_NORMAL, SERVICE_ERROR_SEVERE, and SERVICE_ERROR_CRITICAL.


### -param bstrDependencies [in]

A list of dependencies for the service. There are two possible formats for the string: a standard null-delimited, double-null-terminated string (exactly as documented for <a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>); or a script-friendly list of service names separated by "\" (an invalid character to have in a service name). The rpcss service is implicit in this parameter and does not need to be specified.


### -param bstrRunAs [in]

The user name to run this service as. If this parameter is <b>NULL</b>, the service will run as Local Service.


### -param bstrPassword [in]

The password for the system user account. This parameter must be <b>NULL</b> if the service is configured to run as Local Service.


### -param bDesktopOk [in]

Indicates whether the service should be allowed to interact with the desktop. This parameter is valid only when the service is marked as Local Service and must be <b>FALSE</b> otherwise.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



A service created by this method can be removed using the <a href="https://msdn.microsoft.com/8bc4a72e-79a1-4780-a143-1ba1ec66812b">DeleteServiceForApplication</a> method.




## -see-also




<a href="https://msdn.microsoft.com/ffca611d-dacc-47be-9101-9de76ecc8393">ICOMAdminCatalog2</a>
 

 


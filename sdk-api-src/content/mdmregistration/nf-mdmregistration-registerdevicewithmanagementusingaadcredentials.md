---
UID: NF:mdmregistration.RegisterDeviceWithManagementUsingAADCredentials
title: RegisterDeviceWithManagementUsingAADCredentials function
author: windows-sdk-content
description: Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.
old-location: mdmreg\registerdevicewithmanagementusingaadcredentials.htm
old-project: MDMReg
ms.assetid: 709E464A-C9EC-41EF-AC80-EF0BC35E0905
ms.author: windowssdkdev
ms.date: 02/21/2018
ms.keywords: RegisterDeviceWithManagementUsingAADCredentials, RegisterDeviceWithManagementUsingAADCredentials function [MDM Registration], mdmreg.registerdevicewithmanagementusingaadcredentials, mdmregistration/RegisterDeviceWithManagementUsingAADCredentials
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mdmregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: REGISTRATION_INFORMATION_CLASS, *PREGISTRATION_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MDMRegistration.dll
api_name:
 - RegisterDeviceWithManagementUsingAADCredentials
product: Windows
targetos: Windows
req.lib: MDMRegistration.lib
req.dll: MDMRegistration.dll
req.irql: 
req.product: GDI+ 1.1
---

# RegisterDeviceWithManagementUsingAADCredentials function


## -description


Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.


## -parameters




### -param UserToken [in]

The User to impersonate when attempting to get AAD token


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. If the function fails, the returned value describes the error. Possible 
      values include those listed at 
      <a href="https://msdn.microsoft.com/1f42ed5e-e221-47ec-a019-ed06c05d55d0">MDM Registration Error Values</a>.




## -remarks



The caller of this function must be running as an elevated process.




## -see-also




<a href="https://msdn.microsoft.com/1f42ed5e-e221-47ec-a019-ed06c05d55d0">MDM Registration Error Values</a>



<a href="https://msdn.microsoft.com/1b063a56-f59f-4b02-949f-c8b6bbf45a13">MDM Registration Functions</a>



<a href="https://msdn.microsoft.com/4095197d-40c9-4f51-b28f-fd2fd6d0bba2">UnregisterDeviceWithManagement</a>
 

 


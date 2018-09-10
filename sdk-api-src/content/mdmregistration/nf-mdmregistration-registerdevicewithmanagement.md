---
UID: NF:mdmregistration.RegisterDeviceWithManagement
title: RegisterDeviceWithManagement function
author: windows-sdk-content
description: Registers a device with a MDM service, using the [MS-MDE]:\_Mobile Device Enrollment Protocol.
old-location: mdmreg\registerdevicewithmanagement.htm
tech.root: MDMReg
ms.assetid: 3a927d98-decf-464a-82db-561e9abcfe29
ms.author: windowssdkdev
ms.date: 02/21/2018
ms.keywords: RegisterDeviceWithManagement, RegisterDeviceWithManagement function [MDM Registration], mdmreg.registerdevicewithmanagement, mdmregistration/RegisterDeviceWithManagement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mdmregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
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
req.lib: MDMRegistration.lib
req.dll: MDMRegistration.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MDMRegistration.dll
api_name:
 - RegisterDeviceWithManagement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegisterDeviceWithManagement function


## -description


Registers a device with a MDM service, using the 
    <a href="5c841535-042e-489e-913c-9d783d741267">[MS-MDE]: Mobile Device Enrollment Protocol</a>.


## -parameters




### -param pszUPN [in]

Address of a <b>NULL</b>-terminated Unicode string containing the user principal name 
      (UPN) of the user requesting the registration.

<b>Windows 8.1:  </b>This parameter was located after the <i>ppszMDMServiceUri</i> parameter in Windows 8.1.


### -param ppszMDMServiceUri [in]

Address of a <b>NULL</b>-terminated Unicode string containing the URI of the MDM 
      service.


### -param ppzsAccessToken [in]

Address of a <b>NULL</b>-terminated Unicode string containing a token acquired from 
      a Secure Token Service which the management service will use to validate the user.


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
 

 


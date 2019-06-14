---
UID: NF:mdmregistration.UnregisterDeviceWithManagement
title: UnregisterDeviceWithManagement function (mdmregistration.h)
author: windows-sdk-content
description: Unregisters a device with the MDM service.
old-location: mdmreg\unregisterdevicewithmanagement.htm
tech.root: MDMReg
ms.assetid: 4095197d-40c9-4f51-b28f-fd2fd6d0bba2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UnregisterDeviceWithManagement, UnregisterDeviceWithManagement function [MDM Registration], mdmreg.unregisterdevicewithmanagement, mdmregistration/UnregisterDeviceWithManagement
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
 - UnregisterDeviceWithManagement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UnregisterDeviceWithManagement function


## -description


Unregisters a device with the MDM service


## -parameters




### -param RemoveEnterpriseData [in]

<b>TRUE</b> if resources are to be removed during unregistration, 
      <b>FALSE</b> otherwise.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. If the function 
      fails, the returned value describes the error. Possible 
      values include those listed at 
      <a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>.




## -remarks



The caller of this function must be running as an elevated process.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>



<a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-functions">MDM Registration Functions</a>
 

 


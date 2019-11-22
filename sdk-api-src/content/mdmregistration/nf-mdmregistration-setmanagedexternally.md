---
UID: NF:mdmregistration.SetManagedExternally
title: SetManagedExternally function (mdmregistration.h)

description: Indicates to the MDM agent that the device is managed externally and is not to be registered with an MDM service.
old-location: mdmreg\setmanagedexternally.htm
tech.root: MDMReg
ms.assetid: 6aac0ffb-3502-42a5-b7a3-e11c401543ce

ms.date: 12/05/2018
ms.keywords: SetManagedExternally, SetManagedExternally function [MDM Registration], mdmreg.setmanagedexternally, mdmregistration/SetManagedExternally
ms.topic: function
f1_keywords: 
 - "mdmregistration/SetManagedExternally"
dev_langs:
 - c++
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
 - SetManagedExternally
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetManagedExternally function


## -description


Indicates to the MDM agent that the device is managed externally and is not to be registered with an 
    MDM service.


## -parameters




### -param IsManagedExternally [in]

If <b>TRUE</b> this device is not to be registered with an MDM service. If 
      <b>FALSE</b> this device can be registered with an MDM service.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. If the function fails, the returned value describes the error. Possible 
      values include those listed at 
      <a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>.




## -remarks



The caller of this function must be running as an elevated process.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mdmregistration/nf-mdmregistration-ismanagementregistrationallowed">IsManagementRegistrationAllowed</a>



<a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>



<a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-functions">MDM Registration Functions</a>
 

 


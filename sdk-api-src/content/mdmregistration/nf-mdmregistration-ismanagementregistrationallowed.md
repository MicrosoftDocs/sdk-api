---
UID: NF:mdmregistration.IsManagementRegistrationAllowed
title: IsManagementRegistrationAllowed function
author: windows-sdk-content
description: Checks whether MDM registration is allowed by local policy.
old-location: mdmreg\ismanagementregistrationallowed.htm
old-project: MDMReg
ms.assetid: 138f567d-4c50-4e13-be10-269eb44f9fe5
ms.author: windowssdkdev
ms.date: 02/21/2018
ms.keywords: IsManagementRegistrationAllowed, IsManagementRegistrationAllowed function [MDM Registration], mdmreg.ismanagementregistrationallowed, mdmregistration/IsManagementRegistrationAllowed
ms.prod: windows
ms.technology: windows-sdk
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
 - IsManagementRegistrationAllowed
product: Windows
targetos: Windows
req.lib: MDMRegistration.lib
req.dll: MDMRegistration.dll
req.irql: 
req.product: GDI+ 1.1
---

# IsManagementRegistrationAllowed function


## -description


Checks whether MDM registration is allowed by local policy.


## -parameters




### -param pfIsManagementRegistrationAllowed [out]

Address of a <b>BOOL</b> that receives a value indication whether registration is allowed.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the <b>BOOL</b> pointed to by the <i>pfIsManagementRegistrationAllowed</i> parameter contains <b>TRUE</b> or <b>FALSE</b>. If the function fails, the returned value describes the error. Possible 
      values include those listed at 
      <a href="https://msdn.microsoft.com/1f42ed5e-e221-47ec-a019-ed06c05d55d0">MDM Registration Error Values</a>.




## -remarks



The caller of this function must be running as an elevated process.




## -see-also




<a href="https://msdn.microsoft.com/1f42ed5e-e221-47ec-a019-ed06c05d55d0">MDM Registration Error Values</a>



<a href="https://msdn.microsoft.com/1b063a56-f59f-4b02-949f-c8b6bbf45a13">MDM Registration Functions</a>



<a href="https://msdn.microsoft.com/6aac0ffb-3502-42a5-b7a3-e11c401543ce">SetManagedExternally</a>
 

 


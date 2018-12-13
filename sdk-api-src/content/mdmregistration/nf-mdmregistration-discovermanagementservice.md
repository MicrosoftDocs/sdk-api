---
UID: NF:mdmregistration.DiscoverManagementService
title: DiscoverManagementService function
author: windows-sdk-content
description: Discovers the MDM service.
old-location: mdmreg\discovermanagementservice.htm
tech.root: MDMReg
ms.assetid: 0b01225c-83db-4b13-ad7e-52beae05a8ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DiscoverManagementService, DiscoverManagementService function [MDM Registration], mdmreg.discovermanagementservice, mdmregistration/DiscoverManagementService
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
 - DiscoverManagementService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DiscoverManagementService function


## -description


Discovers the MDM service. The discovery process uses the 
    <a href="https://msdn.microsoft.com/library/Dn409494(v=PROT.20).aspx">[MS-MDE]: Mobile Device Enrollment Protocol</a> 
    protocol.


## -parameters




### -param pszUPN [in]

Address of a <b>NULL</b>-terminated Unicode string containing the user principal name 
      (UPN) of the user requesting registration.


### -param ppMgmtInfo [out]

Address of a <a href="https://msdn.microsoft.com/6be4540b-e74b-41f3-aef4-f613f2a79bab">MANAGEMENT_SERVICE_INFO</a> 
      structure that contains pointers to the URIs of the management and authentication services.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. If the function 
      fails, the returned value describes the error. Possible 
      values include those listed at 
      <a href="https://msdn.microsoft.com/1f42ed5e-e221-47ec-a019-ed06c05d55d0">MDM Registration Error Values</a>.




## -remarks



The caller of this function must be running as an elevated process.




## -see-also




<a href="https://msdn.microsoft.com/6be4540b-e74b-41f3-aef4-f613f2a79bab">MANAGEMENT_SERVICE_INFO</a>



<a href="https://msdn.microsoft.com/1f42ed5e-e221-47ec-a019-ed06c05d55d0">MDM Registration Error Values</a>



<a href="https://msdn.microsoft.com/1b063a56-f59f-4b02-949f-c8b6bbf45a13">MDM Registration Functions</a>
 

 


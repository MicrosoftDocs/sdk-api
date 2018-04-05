---
UID: NF:mdmregistration.DiscoverManagementServiceEx
title: DiscoverManagementServiceEx function
author: windows-driver-content
description: Discovers the MDM service using a candidate server.
old-location: mdmreg\discovermanagementserviceex.htm
old-project: MDMReg
ms.assetid: 600269ff-df88-49ed-b151-df0302cbc4d4
ms.author: windowsdriverdev
ms.date: 2/20/2018
ms.keywords: DiscoverManagementServiceEx, DiscoverManagementServiceEx function [MDM Registration], mdmreg.discovermanagementserviceex, mdmregistration/DiscoverManagementServiceEx
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
req.typenames: REGISTRATION_INFORMATION_CLASS, *PREGISTRATION_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	MDMRegistration.dll
api_name:
-	DiscoverManagementServiceEx
product: Windows
targetos: Windows
req.lib: MDMRegistration.lib
req.dll: MDMRegistration.dll
req.irql: 
req.product: GDI+ 1.1
---

# DiscoverManagementServiceEx function


## -description


Discovers the MDM service using a candidate server. The discovery process uses the 
    <a href="5c841535-042e-489e-913c-9d783d741267">[MS-MDE]: Mobile Device Enrollment Protocol</a> 
    protocol.


## -parameters




### -param pszUPN [in]

Address of a <b>NULL</b>-terminated Unicode string containing the user principal name 
      (UPN) of the user requesting registration.


### -param pszDiscoveryServiceCandidate [in]

Address of a <b>NULL</b>-terminated Unicode string containing the discovery service 
      candidate to use in lieu of automatic discovery.


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

This function is not available before Windows Server 2012 R2 Update and Windows 8.1 Update.




## -see-also




<a href="https://msdn.microsoft.com/0b01225c-83db-4b13-ad7e-52beae05a8ee">DiscoverManagementService</a>



<a href="https://msdn.microsoft.com/6be4540b-e74b-41f3-aef4-f613f2a79bab">MANAGEMENT_SERVICE_INFO</a>



<a href="https://msdn.microsoft.com/1f42ed5e-e221-47ec-a019-ed06c05d55d0">MDM Registration Error Values</a>



<a href="https://msdn.microsoft.com/1b063a56-f59f-4b02-949f-c8b6bbf45a13">MDM Registration Functions</a>
 

 


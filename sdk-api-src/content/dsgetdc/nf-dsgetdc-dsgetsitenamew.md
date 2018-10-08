---
UID: NF:dsgetdc.DsGetSiteNameW
title: DsGetSiteNameW function
author: windows-sdk-content
description: The DsGetSiteName function returns the name of the site where a computer resides.
old-location: ad\dsgetsitename.htm
tech.root: ad
ms.assetid: 2dfffd9a-af4f-4a93-8b3c-966e4f7c455f
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DsGetSiteName, DsGetSiteName function [Active Directory], DsGetSiteNameA, DsGetSiteNameW, _glines_dsgetsitename, ad.dsgetsitename, dsgetdc/DsGetSiteName, dsgetdc/DsGetSiteNameA, dsgetdc/DsGetSiteNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsGetSiteNameW (Unicode) and DsGetSiteNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - DsGetSiteName
 - DsGetSiteNameA
 - DsGetSiteNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsGetSiteNameW function


## -description


The <b>DsGetSiteName</b> function returns the name of the site where a computer resides. For a domain controller (DC), the name of the site is the location of the configured DC. For a member workstation or member server, the name specifies the workstation site as configured in the domain of the computer.


## -parameters




### -param ComputerName [in]

Pointer to a null-terminated string that specifies the name of the server to send this function. A <b>NULL</b> implies the local computer.


### -param SiteName [out]

Pointer to a variable that receives a pointer to a null-terminated string specifying the site location of this computer. This string is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function.


## -returns



If the function returns account information, the return value is <b>NO_ERROR</b>.

If the function fails, the return value can be one of the following error codes.




## -remarks



The <b>DsGetSiteName</b> function does not require any particular access to the specified domain. The function is sent to the "NetLogon" service on the computer specified by <i>ComputerName</i>.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a>



<a href="https://msdn.microsoft.com/bed49e08-4cb7-439c-bfb7-815263ec7568">DsValidateSubnetName</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>
 

 


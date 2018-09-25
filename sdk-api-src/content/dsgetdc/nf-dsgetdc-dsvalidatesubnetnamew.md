---
UID: NF:dsgetdc.DsValidateSubnetNameW
title: DsValidateSubnetNameW function
author: windows-sdk-content
description: The DsValidateSubnetName function validates a subnet name in the form xxx.xxx.xxx.xxx/YY.
old-location: ad\dsvalidatesubnetname.htm
tech.root: ad
ms.assetid: bed49e08-4cb7-439c-bfb7-815263ec7568
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: DsValidateSubnetName, DsValidateSubnetName function [Active Directory], DsValidateSubnetNameA, DsValidateSubnetNameW, _glines_dsvalidatesubnetname, ad.dsvalidatesubnetname, dsgetdc/DsValidateSubnetName, dsgetdc/DsValidateSubnetNameA, dsgetdc/DsValidateSubnetNameW
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
req.unicode-ansi: DsValidateSubnetNameW (Unicode) and DsValidateSubnetNameA (ANSI)
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
 - DsValidateSubnetName
 - DsValidateSubnetNameA
 - DsValidateSubnetNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsValidateSubnetNameW function


## -description


The <b>DsValidateSubnetName</b> function validates a subnet name in the form xxx.xxx.xxx.xxx/YY. The Xxx.xxx.xxx.xxx portion must be a valid IP address. Yy must be the number of leftmost significant bits included in the mask. All bits of the IP address that are not covered by the mask must be specified as zero.


## -parameters




### -param SubnetName [in]

Pointer to a null-terminated string that specifies the name of the subnet to validate.


## -returns



If the function returns account information, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is the following error code.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a>



<a href="https://msdn.microsoft.com/2dfffd9a-af4f-4a93-8b3c-966e4f7c455f">DsGetSiteName</a>
 

 


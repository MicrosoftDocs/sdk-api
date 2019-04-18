---
UID: NF:gpmgmt.IGPM.CreateTrustee
title: IGPM::CreateTrustee (gpmgmt.h)
author: windows-sdk-content
description: Creates and returns a GPMTrustee from which you can retrieve information about a trustee.
old-location: gpmc\igpm_createtrustee.htm
tech.root: gpmc
ms.assetid: 98230e5f-b866-4f68-9977-eec4bdd14d9e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateTrustee, CreateTrustee method [GPMC], CreateTrustee method [GPMC],GPM object, CreateTrustee method [GPMC],IGPM interface, GPM object [GPMC],CreateTrustee method, IGPM interface [GPMC],CreateTrustee method, IGPM.CreateTrustee, IGPM::CreateTrustee, _win32_igpm_createtrustee, gpmc.igpm_createtrustee, gpmgmt/IGPM::CreateTrustee
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPM.CreateTrustee
 - GPM.CreateTrustee
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPM::CreateTrustee


## -description


Creates and returns a <a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">GPMTrustee</a> from which you can retrieve information about a trustee. A trustee is a user, computer, or security group that can be granted permissions on a Group Policy object (GPO), scope of management (SOM), or Windows Management Instrumentation (WMI) filter.


## -parameters




### -param bstrTrustee [in]

Required. Trustee name or the security identifier (SID). Names are in a format that is compatible with Security Accounts Manager (SAM), such as <i>Exampledomain</i>\<i>Someone</i>.


### -param ppIGPMTrustee [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">IGPMTrustee</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">GPMTrustee</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">GPMTrustee</a> object.




## -remarks



For more information about policy-related permissions, see 
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a>. For more information about security groups, see 
<a href="https://msdn.microsoft.com/3236c51f-21c1-4c07-9b76-2668ae72a42f">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">IGPMPermission</a>



<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a>



<a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">IGPMTrustee</a>
 

 


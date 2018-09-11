---
UID: NF:gpmgmt.IGPMGPO.SetSecurityInfo
title: IGPMGPO::SetSecurityInfo
author: windows-sdk-content
description: Sets the list of permissions for the group policy object (GPO), such as who is granted permission to edit it. The method replaces the existing list of permissions.
old-location: gpmc\igpmgpo_setsecurityinfo.htm
tech.root: GPMC
ms.assetid: 52b55e05-6107-4fa7-9991-55550393fee5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMGPO class [GPMC],SetSecurityInfo method, IGPMGPO interface [GPMC],SetSecurityInfo method, IGPMGPO.SetSecurityInfo, IGPMGPO::SetSecurityInfo, SetSecurityInfo, SetSecurityInfo method [GPMC], SetSecurityInfo method [GPMC],GPMGPO class, SetSecurityInfo method [GPMC],IGPMGPO interface, _win32_igpmgpo_setsecurityinfo, gpmc.igpmgpo_setsecurityinfo, gpmgmt/IGPMGPO::SetSecurityInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IGPMGPO.SetSecurityInfo
 - GPMGPO.SetSecurityInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMGPO::SetSecurityInfo


## -description


Sets the list of permissions for the group policy object (GPO), such as who is granted permission to edit it. The method replaces the existing list of permissions.


## -parameters




### -param pSecurityInfo [in]

Pointer to the security information to apply to the GPO.


#### - objGPMSecurityInfo


<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">GPMSecurityInfo</a> object to apply to the GPO.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



For more information about policy-related permissions, see 
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a>.




## -see-also




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a>
 

 


---
UID: NF:gpmgmt.IGPMGPO.GetSecurityInfo
title: IGPMGPO::GetSecurityInfo
author: windows-sdk-content
description: Retrieves the set of permissions for the GPO, such as who is granted permission to edit it.
old-location: gpmc\igpmgpo_getsecurityinfo.htm
old-project: GPMC
ms.assetid: 104e96e6-60c5-4cc1-9728-7c0ea9715a58
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GPMGPO class [GPMC],GetSecurityInfo method, GetSecurityInfo, GetSecurityInfo method [GPMC], GetSecurityInfo method [GPMC],GPMGPO class, GetSecurityInfo method [GPMC],IGPMGPO interface, IGPMGPO interface [GPMC],GetSecurityInfo method, IGPMGPO.GetSecurityInfo, IGPMGPO::GetSecurityInfo, _win32_igpmgpo_getsecurityinfo, gpmc.igpmgpo_getsecurityinfo, gpmgmt/IGPMGPO::GetSecurityInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMGPO.GetSecurityInfo
-	GPMGPO.GetSecurityInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMGPO::GetSecurityInfo


## -description


Retrieves the set of permissions for the GPO, such as who is granted permission to edit it.


## -parameters




### -param ppSecurityInfo [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSecurityInfo</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSecurityInfo</b> object.




## -remarks



For more information about policy-related permissions, see 
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a>.




## -see-also




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a>
 

 


---
UID: NF:gpmgmt.IGPMStarterGPO.SetSecurityInfo
title: IGPMStarterGPO::SetSecurityInfo
author: windows-sdk-content
description: Sets the list of permissions for the Group Policy object (GPO).
old-location: gpmc\igpmstartergpo_setsecurityinfo.htm
old-project: gpmc
ms.assetid: ad4df57f-29b3-4a18-922a-a0d4457703ad
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IGPMStarterGPO interface [GPMC],SetSecurityInfo method, IGPMStarterGPO.SetSecurityInfo, IGPMStarterGPO::SetSecurityInfo, SetSecurityInfo, SetSecurityInfo method [GPMC], SetSecurityInfo method [GPMC],IGPMStarterGPO interface, gpmc.igpmstartergpo_setsecurityinfo, gpmgmt/IGPMStarterGPO::SetSecurityInfo
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gpmgmt.dll
api_name:
 - IGPMStarterGPO.SetSecurityInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMStarterGPO::SetSecurityInfo


## -description


Sets the list of permissions for the Group Policy object (GPO), such as who is granted permission to edit it. The method replaces the existing list of permissions.


## -parameters




### -param pSecurityInfo [in]

Pointer to the security information to apply to the GPO.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



For more information about policy-related permissions, see 
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a>.




## -see-also




<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">IGPMStarterGPO</a>
 

 


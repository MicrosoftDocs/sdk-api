---
UID: NF:gpmgmt.IGPMStarterGPO.GetSecurityInfo
title: IGPMStarterGPO::GetSecurityInfo
author: windows-sdk-content
description: Retrieves the set of permissions for the Starter GPO, such as who is granted permission to edit it.
old-location: gpmc\igpmstartergpo_getsecurityinfo.htm
tech.root: gpmc
ms.assetid: 5c411851-0902-454a-9b44-383ea572ab78
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSecurityInfo, GetSecurityInfo method [GPMC], GetSecurityInfo method [GPMC],IGPMStarterGPO interface, IGPMStarterGPO interface [GPMC],GetSecurityInfo method, IGPMStarterGPO.GetSecurityInfo, IGPMStarterGPO::GetSecurityInfo, gpmc.igpmstartergpo_getsecurityinfo, gpmgmt/IGPMStarterGPO::GetSecurityInfo
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
 - gpmgmt.dll
api_name:
 - IGPMStarterGPO.GetSecurityInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMStarterGPO::GetSecurityInfo


## -description


Retrieves the set of permissions for the Starter GPO, such as who is granted permission to edit it.


## -parameters




### -param ppSecurityInfo [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a> interface.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



For more information about policy-related permissions, see 
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a>.




## -see-also




<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">IGPMStarterGPO</a>
 

 


---
UID: NF:gpmgmt.IGPMSOM.SetSecurityInfo
title: IGPMSOM::SetSecurityInfo
author: windows-sdk-content
description: Sets the list of permissions for the scope of management (SOM) to that of the specified object.
old-location: gpmc\igpmsom_setsecurityinfo.htm
old-project: GPMC
ms.assetid: 675de64c-4eef-47c8-a06c-9167559b11a9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMSOM class [GPMC],SetSecurityInfo method, IGPMSOM interface [GPMC],SetSecurityInfo method, IGPMSOM.SetSecurityInfo, IGPMSOM::SetSecurityInfo, SetSecurityInfo, SetSecurityInfo method [GPMC], SetSecurityInfo method [GPMC],GPMSOM class, SetSecurityInfo method [GPMC],IGPMSOM interface, _win32_igpmsom_setsecurityinfo, gpmc.igpmsom_setsecurityinfo, gpmgmt/IGPMSOM::SetSecurityInfo
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
 - Gpmgmt.dll
api_name:
 - IGPMSOM.SetSecurityInfo
 - GPMSOM.SetSecurityInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMSOM::SetSecurityInfo


## -description


Sets the list of permissions for the scope of management (SOM) to that of the specified object.


## -parameters




### -param pSecurityInfo [in]

Pointer to an 
<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a> interface.


#### - objGPMSecurityInfo


<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">GPMSecurityInfo</a> object to set.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">IGPMPermission</a>



<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">IGPMSOM</a>



<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a>
 

 


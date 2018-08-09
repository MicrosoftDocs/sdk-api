---
UID: NF:gpmgmt.IGPMDomain.GetGPO
title: IGPMDomain::GetGPO
author: windows-sdk-content
description: Retrieves a GPMGPO object with a specified Group Policy object (GPO) ID. The group policy object ID is represented by a GUID.
old-location: gpmc\igpmdomain_getgpo.htm
old-project: GPMC
ms.assetid: ac413241-3649-4f22-9a67-94e4da8672e7
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMDomain object [GPMC],GetGPO method, GetGPO, GetGPO method [GPMC], GetGPO method [GPMC],GPMDomain object, GetGPO method [GPMC],IGPMDomain interface, IGPMDomain interface [GPMC],GetGPO method, IGPMDomain.GetGPO, IGPMDomain::GetGPO, _win32_igpmdomain_getgpo, gpmc.igpmdomain_getgpo, gpmgmt/IGPMDomain::GetGPO
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
 - IGPMDomain.GetGPO
 - GPMDomain.GetGPO
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMDomain::GetGPO


## -description


Retrieves a 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object with a specified Group Policy object (GPO) ID. The group policy object ID is represented by a GUID.


## -parameters




### -param bstrGuid [in]

Required. GUID representing the ID of the group policy object to access. Use null-terminated string.


### -param ppGPO [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> interface for the group policy object ID and domain specified.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 


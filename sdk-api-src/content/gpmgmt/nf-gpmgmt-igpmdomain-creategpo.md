---
UID: NF:gpmgmt.IGPMDomain.CreateGPO
title: IGPMDomain::CreateGPO
author: windows-sdk-content
description: Creates and retrieves a GPMGPO object with a default display name. Typically, the caller sets the display name immediately after calling this method.
old-location: gpmc\igpmdomain_creategpo.htm
tech.root: GPMC
ms.assetid: 00e83637-820b-488e-abf4-4210ac3b98b6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateGPO, CreateGPO method [GPMC], CreateGPO method [GPMC],GPMDomain object, CreateGPO method [GPMC],IGPMDomain interface, GPMDomain object [GPMC],CreateGPO method, IGPMDomain interface [GPMC],CreateGPO method, IGPMDomain.CreateGPO, IGPMDomain::CreateGPO, _win32_igpmdomain_creategpo, gpmc.igpmdomain_creategpo, gpmgmt/IGPMDomain::CreateGPO
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
 - IGPMDomain.CreateGPO
 - GPMDomain.CreateGPO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gpmgmt.h
: 
- IGPMDomain.CreateGPO
: 
---

# IGPMDomain::CreateGPO


## -description


Creates and retrieves a 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object with a default display name. Typically, the caller sets the display name immediately after calling this method.


## -parameters




### -param ppNewGPO

TBD




#### - ppnewGPO [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMGPO</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMGPO</b> object.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 


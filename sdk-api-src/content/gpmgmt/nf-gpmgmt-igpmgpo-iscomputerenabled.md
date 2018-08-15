---
UID: NF:gpmgmt.IGPMGPO.IsComputerEnabled
title: IGPMGPO::IsComputerEnabled
author: windows-sdk-content
description: Checks whether the computer policies in the GPO are enabled.
old-location: gpmc\igpmgpo_iscomputerenabled.htm
old-project: GPMC
ms.assetid: c5e235a0-dc12-4ff5-a3ca-0f3492edb713
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMGPO class [GPMC],IsComputerEnabled method, IGPMGPO interface [GPMC],IsComputerEnabled method, IGPMGPO.IsComputerEnabled, IGPMGPO::IsComputerEnabled, IsComputerEnabled, IsComputerEnabled method [GPMC], IsComputerEnabled method [GPMC],GPMGPO class, IsComputerEnabled method [GPMC],IGPMGPO interface, _win32_igpmgpo_iscomputerenabled, gpmc.igpmgpo_iscomputerenabled, gpmgmt/IGPMGPO::IsComputerEnabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.redist: 
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
 - IGPMGPO.IsComputerEnabled
 - GPMGPO.IsComputerEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMGPO::IsComputerEnabled


## -description


Checks whether the computer policies in the GPO are enabled.


## -parameters




### -param pvbEnabled [out]

Value that indicates whether the computer policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Value that indicates whether the computer policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.

<h3>VB</h3>
Value that indicates whether the computer policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.




## -see-also




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 


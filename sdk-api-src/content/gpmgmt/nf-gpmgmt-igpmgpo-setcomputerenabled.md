---
UID: NF:gpmgmt.IGPMGPO.SetComputerEnabled
title: IGPMGPO::SetComputerEnabled
author: windows-sdk-content
description: Enables or disables the computer settings in the GPO.
old-location: gpmc\igpmgpo_setcomputerenabled.htm
old-project: GPMC
ms.assetid: 22d6fd46-9d6f-455e-8f01-96fc3f44b335
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMGPO class [GPMC],SetComputerEnabled method, IGPMGPO interface [GPMC],SetComputerEnabled method, IGPMGPO.SetComputerEnabled, IGPMGPO::SetComputerEnabled, SetComputerEnabled, SetComputerEnabled method [GPMC], SetComputerEnabled method [GPMC],GPMGPO class, SetComputerEnabled method [GPMC],IGPMGPO interface, _win32_igpmgpo_setcomputerenabled, gpmc.igpmgpo_setcomputerenabled, gpmgmt/IGPMGPO::SetComputerEnabled
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
 - IGPMGPO.SetComputerEnabled
 - GPMGPO.SetComputerEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMGPO::SetComputerEnabled


## -description


Enables or disables the computer settings in the GPO.


## -parameters




### -param vbEnabled






#### - bEnabled [in]

Specifies whether to enable the computer settings in the GPO.

<b>C++:  </b>If <b>VARIANT_TRUE</b>, the method enables the settings; otherwise the method disables them.

<b>Scripting:  </b>If true, the method enables the settings; otherwise the method disables them.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 


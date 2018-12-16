---
UID: NF:gpmgmt.IGPMGPO.SetUserEnabled
title: IGPMGPO::SetUserEnabled
author: windows-sdk-content
description: Enables or disables the user settings in the GPO.
old-location: gpmc\igpmgpo_setuserenabled.htm
tech.root: gpmc
ms.assetid: 25a86f15-a5b0-4412-931b-444f4a684dc6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GPMGPO class [GPMC],SetUserEnabled method, IGPMGPO interface [GPMC],SetUserEnabled method, IGPMGPO.SetUserEnabled, IGPMGPO::SetUserEnabled, SetUserEnabled, SetUserEnabled method [GPMC], SetUserEnabled method [GPMC],GPMGPO class, SetUserEnabled method [GPMC],IGPMGPO interface, _win32_igpmgpo_setuserenabled, gpmc.igpmgpo_setuserenabled, gpmgmt/IGPMGPO::SetUserEnabled
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
 - IGPMGPO.SetUserEnabled
 - GPMGPO.SetUserEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMGPO::SetUserEnabled


## -description


Enables or disables the user settings in the GPO.


## -parameters




### -param vbEnabled [in]

Specifies whether to enable the user settings in the GPO.

<b>C++:  </b>If <b>VARIANT_TRUE</b>, the method enables the settings; otherwise, the method disables them.

<b>Scripting:  </b>If true, the method enables the settings; otherwise, the method disables them.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 


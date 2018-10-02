---
UID: NF:gpmgmt.IGPMGPO.IsUserEnabled
title: IGPMGPO::IsUserEnabled
author: windows-sdk-content
description: Checks whether the user policies in the GPO are enabled.
old-location: gpmc\igpmgpo_isuserenabled.htm
tech.root: GPMC
ms.assetid: a5ed21bd-19b7-4518-97fa-6ffcd4ea80b4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GPMGPO class [GPMC],IsUserEnabled method, IGPMGPO interface [GPMC],IsUserEnabled method, IGPMGPO.IsUserEnabled, IGPMGPO::IsUserEnabled, IsUserEnabled, IsUserEnabled method [GPMC], IsUserEnabled method [GPMC],GPMGPO class, IsUserEnabled method [GPMC],IGPMGPO interface, _win32_igpmgpo_isuserenabled, gpmc.igpmgpo_isuserenabled, gpmgmt/IGPMGPO::IsUserEnabled
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
 - IGPMGPO.IsUserEnabled
 - GPMGPO.IsUserEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMGPO::IsUserEnabled


## -description


Checks whether the user policies in the GPO are enabled.


## -parameters




### -param pvbEnabled [out]

Value that indicates whether the user policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Value that indicates whether the user policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.

<h3>VB</h3>
Value that indicates whether the user policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.




## -see-also




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 


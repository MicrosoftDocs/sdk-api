---
UID: NF:gpmgmt.IGPMGPO.SetWMIFilter
title: IGPMGPO::SetWMIFilter
author: windows-sdk-content
description: Links the GPMWMIFilter object to the current Group Policy object (GPO). This method can also be used to unlink existing WMI filters from the GPO.
old-location: gpmc\igpmgpo_setwmifilter.htm
tech.root: GPMC
ms.assetid: bd086bae-9436-4612-95d6-56fe431d2c51
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GPMGPO class [GPMC],SetWMIFilter method, IGPMGPO interface [GPMC],SetWMIFilter method, IGPMGPO.SetWMIFilter, IGPMGPO::SetWMIFilter, SetWMIFilter, SetWMIFilter method [GPMC], SetWMIFilter method [GPMC],GPMGPO class, SetWMIFilter method [GPMC],IGPMGPO interface, _win32_igpmgpo_setwmifilter, gpmc.igpmgpo_setwmifilter, gpmgmt/IGPMGPO::SetWMIFilter
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
 - IGPMGPO.SetWMIFilter
 - GPMGPO.SetWMIFilter
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
- IGPMGPO.SetWMIFilter
: 
---

# IGPMGPO::SetWMIFilter


## -description


Links the 
<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">GPMWMIFilter</a> object to the current Group Policy object (GPO). This method can also be used to unlink existing WMI filters from the GPO.


## -parameters




### -param pIGPMWMIFilter [in]

Pointer to the WMI filter to associate with the current GPO. Passing <b>NULL</b> in this parameter unlinks any existing WMI filters.


#### - objGPMWMIFilter [in]

<b>GPMWMIFilter</b> object to associate with the current GPO. Passing <b>NULL</b> in this parameter unlinks any existing WMI filters.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>
 

 


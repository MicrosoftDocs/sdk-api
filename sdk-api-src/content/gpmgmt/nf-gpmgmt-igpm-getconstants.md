---
UID: NF:gpmgmt.IGPM.GetConstants
title: IGPM::GetConstants
author: windows-sdk-content
description: Creates and returns a GPMConstants object that allows you to retrieve the value of multiple Group Policy Management Console (GPMC) constants.
old-location: gpmc\igpm_getconstants.htm
tech.root: gpmc
ms.assetid: ba271dbb-320f-409c-aff4-b7dde57f9062
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GPM object [GPMC],GetConstants method, GetConstants, GetConstants method [GPMC], GetConstants method [GPMC],GPM object, GetConstants method [GPMC],IGPM interface, IGPM interface [GPMC],GetConstants method, IGPM.GetConstants, IGPM::GetConstants, _win32_igpm_getconstants, gpmc.igpm_getconstants, gpmgmt/IGPM::GetConstants
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
 - IGPM.GetConstants
 - GPM.GetConstants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPM::GetConstants


## -description


Creates and returns a <a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">GPMConstants</a> object that allows you to retrieve the value of multiple Group Policy Management Console (GPMC) constants.


## -parameters




### -param ppIGPMConstants [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">IGPMConstants</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">GPMConstants</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">GPMConstants</a> object.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">IGPMConstants</a>
 

 


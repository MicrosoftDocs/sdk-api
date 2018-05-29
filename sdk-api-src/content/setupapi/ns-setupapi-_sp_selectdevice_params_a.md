---
UID: NS:setupapi._SP_SELECTDEVICE_PARAMS_A
title: "_SP_SELECTDEVICE_PARAMS_A"
author: windows-sdk-content
description: An SP_SELECTDEVICE_PARAMS structure corresponds to a DIF_SELECTDEVICE installation request.
old-location: devinst\sp_selectdevice_params.htm
old-project: devinst
ms.assetid: 7d1168dd-0b61-44fb-928d-38f2c57c1092
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PSP_SELECTDEVICE_PARAMS_A, PSP_SELECTDEVICE_PARAMS, PSP_SELECTDEVICE_PARAMS structure pointer [Device and Driver Installation], SP_SELECTDEVICE_PARAMS, SP_SELECTDEVICE_PARAMS structure [Device and Driver Installation], SP_SELECTDEVICE_PARAMS_A, _SP_SELECTDEVICE_PARAMS_A, devinst.sp_selectdevice_params, di-struct_897a5d1d-5ff3-4d70-b39d-3763b81d54bf.xml, setupapi/PSP_SELECTDEVICE_PARAMS, setupapi/SP_SELECTDEVICE_PARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SP_SELECTDEVICE_PARAMS_A, *PSP_SELECTDEVICE_PARAMS_A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	setupapi.h
api_name:
-	SP_SELECTDEVICE_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _SP_SELECTDEVICE_PARAMS_A structure


## -description


An SP_SELECTDEVICE_PARAMS structure corresponds to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff543723">DIF_SELECTDEVICE</a> installation request.


## -struct-fields




### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a>. 


### -field Title

Buffer that contains an installer-provided window title for driver-selection windows. Windows uses this title for the window title for the Select Device dialogs. 


### -field Instructions

Buffer that contains an installer-provided select-device instructions. 


### -field ListLabel

Buffer that contains an installer-provided label for the list of drivers from which the user can select.


### -field SubTitle

Buffer that contains an installer-provided subtitle used in select-device wizards. This string is not used in select dialogs.


### -field Reserved

Reserved. For internal use only.


## -remarks



If an installer sets fields in this structure to be used during driver selection, the installer must also set the DI_USECI_SELECTSTRINGS flag in the SP_DEVINSTALL_PARAMS. 

The following screen shot shows a sample Select Device dialog box and identifies the strings an installer can supply.

<img alt="Screen shot of a Select a Device Driver dialog box" src="images/select-dialog.png"/>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543723">DIF_SELECTDEVICE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552115">SetupDiSelectDevice</a>
 

 


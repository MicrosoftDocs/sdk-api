---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 


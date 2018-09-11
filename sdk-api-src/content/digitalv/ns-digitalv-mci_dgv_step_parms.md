---
UID: NS:digitalv.MCI_DGV_STEP_PARMS
title: MCI_DGV_STEP_PARMS
author: windows-sdk-content
description: The MCI_DGV_STEP_PARMS structure contains parameters for the MCI_STEP command for digital-video devices.
old-location: multimedia\mci_dgv_step_parms.htm
tech.root: Multimedia
ms.assetid: 479e68e8-7c0b-4a28-b0c2-eea12af6843e
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: "*LPMCI_DGV_STEP_PARMS, MCI_DGV_STEP_PARMS, MCI_DGV_STEP_PARMS structure [Windows Multimedia], _win32_MCI_DGV_STEP_PARMS_str, digitalv/MCI_DGV_STEP_PARMS, multimedia.mci_dgv_step_parms"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: digitalv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Digitalv.h
api_name:
 - MCI_DGV_STEP_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_STEP_PARMS
req.redist: 
---

# MCI_DGV_STEP_PARMS structure


## -description



The <b>MCI_DGV_STEP_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/8d976840-fe9d-4393-b9fc-10f847166b1b">MCI_STEP</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwFrames

Number of frames to step.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/8d976840-fe9d-4393-b9fc-10f847166b1b">MCI_STEP</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


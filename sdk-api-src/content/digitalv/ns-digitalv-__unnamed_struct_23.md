---
UID: NS:digitalv.__unnamed_struct_23
title: MCI_DGV_SAVE_PARMSW
author: windows-sdk-content
description: The MCI_DGV_SAVE_PARMS structure contains information for the MCI_SAVE command for digital-video devices.
old-location: multimedia\mci_dgv_save_parms.htm
tech.root: Multimedia
ms.assetid: a647099c-f5f8-4728-99a1-8b5b8c6b67bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPMCI_DGV_SAVE_PARMSW, MCI_DGV_SAVE_PARMS, MCI_DGV_SAVE_PARMS structure [Windows Multimedia], MCI_DGV_SAVE_PARMSW, _win32_MCI_DGV_SAVE_PARMS_str, digitalv/MCI_DGV_SAVE_PARMS, multimedia.mci_dgv_save_parms"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MCI_DGV_SAVE_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_SAVE_PARMSW
req.redist: 
---

# MCI_DGV_SAVE_PARMSW structure


## -description



The <b>MCI_DGV_SAVE_PARMS</b> structure contains information for the <a href="https://msdn.microsoft.com/286e6f31-cb93-443b-8191-8c363b366eae">MCI_SAVE</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field lpstrFileName

String for filename to save.


### -field rc

Rectangle containing positioning information. <a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/286e6f31-cb93-443b-8191-8c363b366eae">MCI_SAVE</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


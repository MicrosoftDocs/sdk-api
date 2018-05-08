---
UID: NS:digitalv.MCI_DGV_RESTORE_PARMSA
title: MCI_DGV_RESTORE_PARMSA
author: windows-driver-content
description: The MCI_DGV_RESTORE_PARMS structure contains information for the MCI_RESTORE command for digital-video devices.
old-location: multimedia\mci_dgv_restore_parms.htm
old-project: Multimedia
ms.assetid: 2b8fb9a8-b7a2-4775-a21e-0ebcb2c96b24
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: "*LPMCI_DGV_RESTORE_PARMSA, MCI_DGV_RESTORE_PARMS, MCI_DGV_RESTORE_PARMS structure [Windows Multimedia], MCI_DGV_RESTORE_PARMSA, _win32_MCI_DGV_RESTORE_PARMS_str, digitalv/MCI_DGV_RESTORE_PARMS, multimedia.mci_dgv_restore_parms"
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
req.typenames: MCI_DGV_RESTORE_PARMSA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Digitalv.h
api_name:
-	MCI_DGV_RESTORE_PARMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MCI_DGV_RESTORE_PARMSA structure


## -description



The <b>MCI_DGV_RESTORE_PARMS</b> structure contains information for the <a href="https://msdn.microsoft.com/ed309cc6-72a3-4abb-aef2-40a55381d8b6">MCI_RESTORE</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field lpstrFileName

Pointer to a null-terminated string containing the filename from which the frame buffer information will be restored.


### -field ptOffset

 


### -field ptExtent

 


### -field rc

Rectangle containing positioning information. <a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/ed309cc6-72a3-4abb-aef2-40a55381d8b6">MCI_RESTORE</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


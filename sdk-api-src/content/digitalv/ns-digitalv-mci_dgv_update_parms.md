---
UID: NS:digitalv.__unnamed_struct_33
title: MCI_DGV_UPDATE_PARMS
author: windows-sdk-content
description: The MCI_DGV_UPDATE_PARMS structure contains parameters for the MCI_UPDATE command.
old-location: multimedia\mci_dgv_update_parms.htm
tech.root: Multimedia
ms.assetid: 66289ff2-0e8c-4320-997c-b5078fc6db12
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPMCI_DGV_UPDATE_PARMS, MCI_DGV_UPDATE_PARMS, MCI_DGV_UPDATE_PARMS structure [Windows Multimedia], _win32_MCI_DGV_UPDATE_PARMS_str, digitalv/MCI_DGV_UPDATE_PARMS, multimedia.mci_dgv_update_parms"
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
 - MCI_DGV_UPDATE_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_UPDATE_PARMS
req.redist: 
---

# MCI_DGV_UPDATE_PARMS structure


## -description



The <b>MCI_DGV_UPDATE_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/90a8c10f-61b9-49a1-bbcc-e0729aa8c454">MCI_UPDATE</a> command.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field ptOffset

 


### -field ptExtent

 


### -field rc

Rectangle containing positioning information. <a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.


### -field hDC

Handle to display context.


### -field wReserved0

 




## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/90a8c10f-61b9-49a1-bbcc-e0729aa8c454">MCI_UPDATE</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


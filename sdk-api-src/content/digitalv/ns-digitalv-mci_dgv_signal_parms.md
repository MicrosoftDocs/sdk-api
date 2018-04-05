---
UID: NS:digitalv.MCI_DGV_SIGNAL_PARMS
title: MCI_DGV_SIGNAL_PARMS
author: windows-driver-content
description: The MCI_DGV_SIGNAL_PARMS structure contains parameters for the MCI_SIGNAL command for digital-video devices.
old-location: multimedia\mci_dgv_signal_parms.htm
old-project: Multimedia
ms.assetid: 01076be3-6eaa-4fa3-a676-1698a9c08271
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPMCI_DGV_SIGNAL_PARMS, MCI_DGV_SIGNAL_PARMS, MCI_DGV_SIGNAL_PARMS structure [Windows Multimedia], _win32_MCI_DGV_SIGNAL_PARMS_str, digitalv/MCI_DGV_SIGNAL_PARMS, multimedia.mci_dgv_signal_parms"
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
req.typenames: MCI_DGV_SIGNAL_PARMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Digitalv.h
api_name:
-	MCI_DGV_SIGNAL_PARMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MCI_DGV_SIGNAL_PARMS structure


## -description



The <b>MCI_DGV_SIGNAL_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/32ca21a0-e2df-47f1-8e13-67c9d8f149db">MCI_SIGNAL</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwPosition

Position to be marked.


### -field dwPeriod

Interval of the position marks.


### -field dwUserParm

User value associated with signals.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/32ca21a0-e2df-47f1-8e13-67c9d8f149db">MCI_SIGNAL</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


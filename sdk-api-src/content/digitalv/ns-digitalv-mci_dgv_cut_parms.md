---
UID: NS:digitalv.MCI_DGV_CUT_PARMS
title: MCI_DGV_CUT_PARMS
author: windows-sdk-content
description: The MCI_DGV_CUT_PARMS structure contains parameters for the MCI_CUT command for digital-video devices.
old-location: multimedia\mci_dgv_cut_parms.htm
tech.root: Multimedia
ms.assetid: fe3e2bbb-7874-421d-90ca-f7d718cd8c27
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*LPMCI_DGV_CUT_PARMS, MCI_DGV_CUT_PARMS, MCI_DGV_CUT_PARMS structure [Windows Multimedia], _win32_MCI_DGV_CUT_PARMS_str, digitalv/MCI_DGV_CUT_PARMS, multimedia.mci_dgv_cut_parms"
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
 - MCI_DGV_CUT_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_CUT_PARMS
req.redist: 
---

# MCI_DGV_CUT_PARMS structure


## -description



The <b>MCI_DGV_CUT_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/09bb505b-715a-4393-80f0-e9ba270a8ac1">MCI_CUT</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwFrom

Starting position for cut.


### -field dwTo

Ending position for cut.


### -field ptOffset

 


### -field ptExtent

 


### -field rc

Rectangle describing area to be cut. <a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.


### -field dwAudioStream

Audio stream.


### -field dwVideoStream

Video stream.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/09bb505b-715a-4393-80f0-e9ba270a8ac1">MCI_CUT</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


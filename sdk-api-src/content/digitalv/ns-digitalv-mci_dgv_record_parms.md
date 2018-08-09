---
UID: NS:digitalv.MCI_DGV_RECORD_PARMS
title: MCI_DGV_RECORD_PARMS
author: windows-sdk-content
description: The MCI_DGV_RECORD_PARMS structure contains parameters for the MCI_RECORD command for digital-video devices.
old-location: multimedia\mci_dgv_record_parms.htm
old-project: Multimedia
ms.assetid: c0a537b1-d38c-41fa-8bd7-bee90ac625a7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPMCI_DGV_RECORD_PARMS, MCI_DGV_RECORD_PARMS, MCI_DGV_RECORD_PARMS structure [Windows Multimedia], _win32_MCI_DGV_RECORD_PARMS_str, digitalv/MCI_DGV_RECORD_PARMS, multimedia.mci_dgv_record_parms"
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
tech.root: 
req.typenames: MCI_DGV_RECORD_PARMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Digitalv.h
api_name:
 - MCI_DGV_RECORD_PARMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MCI_DGV_RECORD_PARMS structure


## -description



The <b>MCI_DGV_RECORD_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02">MCI_RECORD</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwFrom

Position to record from.


### -field dwTo

Position to record to.


### -field ptOffset

 


### -field ptExtent

 


### -field rc

The region of the frame buffer used as the source for the pixels compressed and saved. <a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.


### -field dwAudioStream

Audio stream.


### -field dwVideoStream

Video stream.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02">MCI_RECORD</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


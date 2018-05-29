---
UID: NS:digitalv.MCI_DGV_SET_PARMS
title: MCI_DGV_SET_PARMS
author: windows-sdk-content
description: The MCI_DGV_SET_PARMS structure contains parameters for the MCI_SET command for digital-video devices.
old-location: multimedia\mci_dgv_set_parms.htm
old-project: Multimedia
ms.assetid: 1dd44f82-0890-4485-91bf-e418e6369b2a
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPMCI_DGV_SET_PARMS, MCI_DGV_SET_PARMS, MCI_DGV_SET_PARMS structure [Windows Multimedia], _win32_MCI_DGV_SET_PARMS_str, digitalv/MCI_DGV_SET_PARMS, multimedia.mci_dgv_set_parms"
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
req.typenames: MCI_DGV_SET_PARMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Digitalv.h
api_name:
-	MCI_DGV_SET_PARMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MCI_DGV_SET_PARMS structure


## -description



The <b>MCI_DGV_SET_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/c527f9d6-2119-4274-98b7-dc892e9b70f9">MCI_SET</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwTimeFormat

Time format of device.


### -field dwAudio

Channel for audio output.


### -field dwFileFormat

File format.


### -field dwSpeed

Playback speed.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/c527f9d6-2119-4274-98b7-dc892e9b70f9">MCI_SET</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


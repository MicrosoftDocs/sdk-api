---
UID: NS:digitalv.__unnamed_struct_25
title: MCI_DGV_SETAUDIO_PARMSA
author: windows-sdk-content
description: The MCI_DGV_SETAUDIO_PARMS structure contains parameters for the MCI_SETAUDIO command for digital-video devices.
old-location: multimedia\mci_dgv_setaudio_parms.htm
tech.root: Multimedia
ms.assetid: 9c2e72d0-5f6a-4884-a072-ed3d38b953c5
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "*LPMCI_DGV_SETAUDIO_PARMSA, MCI_DGV_SETAUDIO_PARMS, MCI_DGV_SETAUDIO_PARMS structure [Windows Multimedia], MCI_DGV_SETAUDIO_PARMSA, _win32_MCI_DGV_SETAUDIO_PARMS_str, digitalv/MCI_DGV_SETAUDIO_PARMS, multimedia.mci_dgv_setaudio_parms"
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
 - MCI_DGV_SETAUDIO_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_SETAUDIO_PARMSA
req.redist: 
---

# MCI_DGV_SETAUDIO_PARMSA structure


## -description



The <b>MCI_DGV_SETAUDIO_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/78624596-e465-4ef1-8988-edcfe9a46f89">MCI_SETAUDIO</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwItem

Constant indicating the target adjustment. For a list of possible values, see the <a href="https://msdn.microsoft.com/78624596-e465-4ef1-8988-edcfe9a46f89">MCI_SETAUDIO</a> command.


### -field dwValue

Adjustment level.


### -field dwOver

Transmission length.


### -field lpstrAlgorithm

Pointer to a null-terminated string containing the name of the audio-compression algorithm.


### -field lpstrQuality

Pointer to a null-terminated string containing a descriptor of the audio-compression algorithm.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/78624596-e465-4ef1-8988-edcfe9a46f89">MCI_SETAUDIO</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


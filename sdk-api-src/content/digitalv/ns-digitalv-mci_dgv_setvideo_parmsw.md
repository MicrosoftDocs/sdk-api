---
UID: NS:digitalv.MCI_DGV_SETVIDEO_PARMSW
title: MCI_DGV_SETVIDEO_PARMSW
author: windows-sdk-content
description: The MCI_DGV_SETVIDEO_PARMS structure contains parameters for the MCI_SETVIDEO command for digital-video devices.
old-location: multimedia\mci_dgv_setvideo_parms.htm
tech.root: Multimedia
ms.assetid: 1ecc41b9-6c09-4ebb-b14a-e4044df3b5b7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*LPMCI_DGV_SETVIDEO_PARMSW, MCI_DGV_SETVIDEO_PARMS, MCI_DGV_SETVIDEO_PARMS structure [Windows Multimedia], MCI_DGV_SETVIDEO_PARMSW, _win32_MCI_DGV_SETVIDEO_PARMS_str, digitalv/MCI_DGV_SETVIDEO_PARMS, multimedia.mci_dgv_setvideo_parms"
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
 - MCI_DGV_SETVIDEO_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_SETVIDEO_PARMSW
req.redist: 
---

# MCI_DGV_SETVIDEO_PARMSW structure


## -description



The <b>MCI_DGV_SETVIDEO_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/b84956d8-01a0-49f6-a96c-2693a25e6f2a">MCI_SETVIDEO</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwItem

Constant indicating the target adjustment.


### -field dwValue

Adjustment level.


### -field dwOver

Transmission length.


### -field lpstrAlgorithm

Pointer to a null-terminated string containing the name of the video-compression algorithm.


### -field lpstrQuality

Pointer to a null-terminated string containing a descriptor of the video-compression algorithm.


### -field dwSourceNumber

Index of input source.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/b84956d8-01a0-49f6-a96c-2693a25e6f2a">MCI_SETVIDEO</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


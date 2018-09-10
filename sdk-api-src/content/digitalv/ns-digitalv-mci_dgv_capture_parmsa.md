---
UID: NS:digitalv.MCI_DGV_CAPTURE_PARMSA
title: MCI_DGV_CAPTURE_PARMSA
author: windows-sdk-content
description: The MCI_DGV_CAPTURE_PARMS structure contains parameters for the MCI_CAPTURE command for digital-video devices.
old-location: multimedia\mci_dgv_capture_parms.htm
tech.root: Multimedia
ms.assetid: 8ab62c4b-6db2-4a52-b015-a1d635e1edd4
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: "*LPMCI_DGV_CAPTURE_PARMSA, MCI_DGV_CAPTURE_PARMS, MCI_DGV_CAPTURE_PARMS structure [Windows Multimedia], MCI_DGV_CAPTURE_PARMSA, _win32_MCI_DGV_CAPTURE_PARMS_str, digitalv/MCI_DGV_CAPTURE_PARMS, multimedia.mci_dgv_capture_parms"
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
 - MCI_DGV_CAPTURE_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_CAPTURE_PARMSA
req.redist: 
---

# MCI_DGV_CAPTURE_PARMSA structure


## -description



The <b>MCI_DGV_CAPTURE_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/bdebddc5-a0a0-449e-889e-37c7d6612c60">MCI_CAPTURE</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field lpstrFileName

Pointer to a null-terminated string specifying the destination path and filename for the file that receives the captured data.


### -field ptOffset

 


### -field ptExtent

 


### -field rc

Rectangle containing positioning information. <a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <b>mciSendCommand</b> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


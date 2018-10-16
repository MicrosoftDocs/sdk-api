---
UID: NS:digitalv.MCI_DGV_RECT_PARMS
title: MCI_DGV_RECT_PARMS
author: windows-sdk-content
description: The MCI_DGV_RECT_PARMS structure contains parameters for the MCI_FREEZE, MCI_PUT, MCI_UNFREEZE, and MCI_WHERE commands for digital-video devices.
old-location: multimedia\mci_dgv_rect_parms.htm
tech.root: Multimedia
ms.assetid: b73e6344-f5d8-4d21-bda9-ac076bf79dc8
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*LPMCI_DGV_FREEZE_PARMS, *LPMCI_DGV_PUT_PARMS, *LPMCI_DGV_RECT_PARMS, *LPMCI_DGV_UNFREEZE_PARMS, *LPMCI_DGV_WHERE_PARMS, MCI_DGV_FREEZE_PARMS, MCI_DGV_PUT_PARMS, MCI_DGV_RECT_PARMS, MCI_DGV_RECT_PARMS structure [Windows Multimedia], MCI_DGV_UNFREEZE_PARMS, MCI_DGV_WHERE_PARMS, _win32_MCI_DGV_RECT_PARMS_str, digitalv/MCI_DGV_RECT_PARMS, multimedia.mci_dgv_rect_parms"
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
 - MCI_DGV_RECT_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_RECT_PARMS
req.redist: 
---

# MCI_DGV_RECT_PARMS structure


## -description



The <b>MCI_DGV_RECT_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/6f90984a-24dc-4046-8234-986b2125bab4">MCI_FREEZE</a>, <a href="https://msdn.microsoft.com/9d81682b-6546-4e6d-a6df-e2de8c013b66">MCI_PUT</a>, <a href="https://msdn.microsoft.com/79ff1be5-6e30-4ef4-ab81-fc5643e3a72d">MCI_UNFREEZE</a>, and <a href="https://msdn.microsoft.com/f64a7e49-4ee1-4836-ba9a-0bbdc47626b3">MCI_WHERE</a> commands for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field ptOffset

 


### -field ptExtent

 


### -field rc

Rectangle containing positioning information. <a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.


## -remarks



The <a href="https://msdn.microsoft.com/66dc6390-b966-43bf-a044-1c98b47479c8">MCI_DGV_FREEZE_PARMS</a>, <a href="https://msdn.microsoft.com/d7c1a0fd-7228-4dbb-bf84-273f2677388a">MCI_DGV_PUT_PARMS</a>, <b>MCI_DGV_UNFREEZE_PARMS</b> and <b>MCI_DGV_WHERE_PARMS</b> structures are identical to the <b>MCI_DGV_RECT_PARMS</b> structure.

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/6f90984a-24dc-4046-8234-986b2125bab4">MCI_FREEZE</a>



<a href="https://msdn.microsoft.com/9d81682b-6546-4e6d-a6df-e2de8c013b66">MCI_PUT</a>



<a href="https://msdn.microsoft.com/79ff1be5-6e30-4ef4-ab81-fc5643e3a72d">MCI_UNFREEZE</a>



<a href="https://msdn.microsoft.com/f64a7e49-4ee1-4836-ba9a-0bbdc47626b3">MCI_WHERE</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=16998">RECT</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


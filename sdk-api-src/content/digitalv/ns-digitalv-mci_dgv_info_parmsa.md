---
UID: NS:digitalv.MCI_DGV_INFO_PARMSA
title: MCI_DGV_INFO_PARMSA
author: windows-sdk-content
description: The MCI_DGV_INFO_PARMS structure contains parameters for the MCI_INFO command for digital-video devices.
old-location: multimedia\mci_dgv_info_parms.htm
old-project: Multimedia
ms.assetid: 812a2445-d7a0-4751-8af5-7c9d5e673e27
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPMCI_DGV_INFO_PARMSA, MCI_DGV_INFO_PARMS, MCI_DGV_INFO_PARMS structure [Windows Multimedia], MCI_DGV_INFO_PARMSA, _win32_MCI_DGV_INFO_PARMS_str, digitalv/MCI_DGV_INFO_PARMS, multimedia.mci_dgv_info_parms"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: digitalv.h
req.include-header: 
req.redist: 
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
req.typenames: MCI_DGV_INFO_PARMSA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Digitalv.h
api_name:
 - MCI_DGV_INFO_PARMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MCI_DGV_INFO_PARMSA structure


## -description



The <b>MCI_DGV_INFO_PARMS</b> structure contains parameters for the <a href="https://msdn.microsoft.com/aed3fed3-87b9-4673-9171-4f57770d765c">MCI_INFO</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field lpstrReturn

Pointer to buffer for return string.


### -field dwRetSize

Size, in bytes, of return buffer.


### -field dwItem

Constant describing information to return.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/aed3fed3-87b9-4673-9171-4f57770d765c">MCI_INFO</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


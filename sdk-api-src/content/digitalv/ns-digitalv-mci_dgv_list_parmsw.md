---
UID: NS:digitalv.MCI_DGV_LIST_PARMSW
title: MCI_DGV_LIST_PARMSW
author: windows-sdk-content
description: The MCI_DGV_LIST_PARMS structure contains the information for the MCI_LIST command for digital-video devices.
old-location: multimedia\mci_dgv_list_parms.htm
old-project: Multimedia
ms.assetid: f1b44fca-6c33-4883-911c-7b18fc3084c2
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: "*LPMCI_DGV_LIST_PARMSW, MCI_DGV_LIST_PARMS, MCI_DGV_LIST_PARMS structure [Windows Multimedia], MCI_DGV_LIST_PARMSW, _win32_MCI_DGV_LIST_PARMS_str, digitalv/MCI_DGV_LIST_PARMS, multimedia.mci_dgv_list_parms"
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
req.typenames: MCI_DGV_LIST_PARMSW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Digitalv.h
api_name:
 - MCI_DGV_LIST_PARMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MCI_DGV_LIST_PARMSW structure


## -description



The <b>MCI_DGV_LIST_PARMS</b> structure contains the information for the <a href="https://msdn.microsoft.com/1977fbfa-cae4-4afe-9fc5-ac68177574ca">MCI_LIST</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field lpstrReturn

Buffer for return string.


### -field dwLength

Length, in bytes, of buffer.


### -field dwNumber

Index of item in list.


### -field dwItem

Type of list item.


### -field lpstrAlgorithm

String containing algorithm name.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://msdn.microsoft.com/b414dffb-3701-4dfd-aa8c-cd8e8918027d">MCI</a>



<a href="https://msdn.microsoft.com/e86740e5-633e-465d-94ef-8065a8c05b31">MCI Structures</a>



<a href="https://msdn.microsoft.com/1977fbfa-cae4-4afe-9fc5-ac68177574ca">MCI_LIST</a>



<a href="https://msdn.microsoft.com/e25820e9-2caf-423e-8588-f842e670e0c3">mciSendCommand</a>
 

 


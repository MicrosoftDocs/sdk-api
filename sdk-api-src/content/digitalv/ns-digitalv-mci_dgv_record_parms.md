---
UID: NS:digitalv.__unnamed_struct_17
title: MCI_DGV_RECORD_PARMS (digitalv.h)
description: The MCI_DGV_RECORD_PARMS structure contains parameters for the MCI_RECORD command for digital-video devices.
helpviewer_keywords: ["*LPMCI_DGV_RECORD_PARMS","MCI_DGV_RECORD_PARMS","MCI_DGV_RECORD_PARMS structure [Windows Multimedia]","_win32_MCI_DGV_RECORD_PARMS_str","digitalv/MCI_DGV_RECORD_PARMS","multimedia.mci_dgv_record_parms"]
old-location: multimedia\mci_dgv_record_parms.htm
tech.root: Multimedia
ms.assetid: c0a537b1-d38c-41fa-8bd7-bee90ac625a7
ms.date: 12/05/2018
ms.keywords: '*LPMCI_DGV_RECORD_PARMS, MCI_DGV_RECORD_PARMS, MCI_DGV_RECORD_PARMS structure [Windows Multimedia], _win32_MCI_DGV_RECORD_PARMS_str, digitalv/MCI_DGV_RECORD_PARMS, multimedia.mci_dgv_record_parms'
f1_keywords:
- digitalv/MCI_DGV_RECORD_PARMS
dev_langs:
- c++
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
- MCI_DGV_RECORD_PARMS
targetos: Windows
req.typenames: MCI_DGV_RECORD_PARMS
req.redist: 
ms.custom: 19H1
---

# MCI_DGV_RECORD_PARMS structure


## -description



The <b>MCI_DGV_RECORD_PARMS</b> structure contains parameters for the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-record">MCI_RECORD</a> command for digital-video devices.




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

The region of the frame buffer used as the source for the pixels compressed and saved. <a href="https://msdn.microsoft.com/library/ms536136.aspx">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.


### -field dwAudioStream

Audio stream.


### -field dwVideoStream

Video stream.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://docs.microsoft.com/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci">MCI</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-record">MCI_RECORD</a>



<a href="https://msdn.microsoft.com/library/ms536136.aspx">RECT</a>



<a href="https://docs.microsoft.com/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>
 

 


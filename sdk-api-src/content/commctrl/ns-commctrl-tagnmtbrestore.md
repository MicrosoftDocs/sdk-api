---
UID: NS:commctrl.tagNMTBRESTORE
title: tagNMTBRESTORE
author: windows-sdk-content
description: Allows applications to extract the information that was placed in NMTBSAVE when the toolbar state was saved. This structure is passed to applications when they receive a TBN_RESTORE notification code.
old-location: controls\NMTBRESTORE.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtbrestore.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: "*LPNMTBRESTORE, LPNMTBRESTORE, LPNMTBRESTORE structure pointer [Windows Controls], NMTBRESTORE, NMTBRESTORE structure [Windows Controls], _win32_NMTBRESTORE, _win32_NMTBRESTORE_cpp, commctrl/LPNMTBRESTORE, commctrl/NMTBRESTORE, controls.NMTBRESTORE, controls._win32_NMTBRESTORE, tagNMTBRESTORE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: NMTBRESTORE, *LPNMTBRESTORE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMTBRESTORE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagNMTBRESTORE structure


## -description


Allows applications to extract the information that was placed in <a href="https://msdn.microsoft.com/6cfad7d3-6730-4f03-8804-b44ea4d9bbd7">NMTBSAVE</a> when the toolbar state was saved. This structure is passed to applications when they receive a <a href="https://msdn.microsoft.com/b1f0c801-d56b-4e93-b9ba-b572aaa38647">TBN_RESTORE</a> notification code.


## -struct-fields




### -field hdr

 


### -field pData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer to the data stream with the stored save information. It contains Shell-defined blocks of information for each button, alternating with application-defined blocks. Applications may also place a block of global data at the start of 
					<b>pData</b>. The format and length of the application-defined blocks are determined by the application. 


### -field pCurrent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer to the current block of application-defined data. After extracting the data, the application must advance 
					<b>pCurrent</b> to the end of the block, so it is pointing to the next block of Shell-defined data. 


### -field cbData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of 
					<b>pData</b>. 


### -field iItem

Type: <b>int</b>

Value of -1 indicates that the restore is starting, and 
					<b>pCurrent</b> will point to the start of the data stream. Otherwise, it is the zero-based button index, and 
					<b>pCurrent</b> will point to the current button's data. 


### -field cButtons

Type: <b>int</b>

Estimate of the number of buttons. Because the estimate is based on the size of the data stream, it might be incorrect. The client should update it as appropriate. 


### -field cbBytesPerRecord

Type: <b>int</b>

Number of bytes needed to hold the data for each button. When the restore starts, 
					<b>cbBytesPerRecord</b> will be set to the size of the Shell-defined data structure. You need to increment it by the size of the structure that holds the application-defined data.


### -field tbButton

Type: <b><a href="https://msdn.microsoft.com/c7dea982-d8b3-44e1-a4d2-3cca560c2096">TBBUTTON</a></b>


<a href="https://msdn.microsoft.com/c7dea982-d8b3-44e1-a4d2-3cca560c2096">TBBUTTON</a> structure that contains information about the button currently being restored. Applications must modify this structure as necessary before returning. 


#### - nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


---
UID: NS:commctrl.tagNMTBRESTORE
title: tagNMTBRESTORE
author: windows-sdk-content
description: Allows applications to extract the information that was placed in NMTBSAVE when the toolbar state was saved. This structure is passed to applications when they receive a TBN_RESTORE notification code.
old-location: controls\NMTBRESTORE.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtbrestore.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: NMTBRESTORE, *LPNMTBRESTORE
req.redist: 
---

# tagNMTBRESTORE structure


## -description


Allows applications to extract the information that was placed in <a href="https://msdn.microsoft.com/en-us/library/Bb760471(v=VS.85).aspx">NMTBSAVE</a> when the toolbar state was saved. This structure is passed to applications when they receive a <a href="https://msdn.microsoft.com/en-us/library/Bb787283(v=VS.85).aspx">TBN_RESTORE</a> notification code.


## -struct-fields




### -field hdr

 


### -field pData

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD</a>*</b>

Pointer to the data stream with the stored save information. It contains Shell-defined blocks of information for each button, alternating with application-defined blocks. Applications may also place a block of global data at the start of 
					<b>pData</b>. The format and length of the application-defined blocks are determined by the application. 


### -field pCurrent

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD</a>*</b>

Pointer to the current block of application-defined data. After extracting the data, the application must advance 
					<b>pCurrent</b> to the end of the block, so it is pointing to the next block of Shell-defined data. 


### -field cbData

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb760476(v=VS.85).aspx">TBBUTTON</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb760476(v=VS.85).aspx">TBBUTTON</a> structure that contains information about the button currently being restored. Applications must modify this structure as necessary before returning. 


#### - nmhdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about the notification. 


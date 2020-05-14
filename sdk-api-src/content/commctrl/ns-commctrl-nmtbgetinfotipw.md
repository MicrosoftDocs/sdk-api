---
UID: NS:commctrl.tagNMTBGETINFOTIPW
title: NMTBGETINFOTIPW (commctrl.h)
description: Contains and receives infotip information for a toolbar item. This structure is used with the TBN_GETINFOTIP notification code.helpviewer_keywords: ["*LPNMTBGETINFOTIPW","LPNMTBGETINFOTIP","LPNMTBGETINFOTIP structure pointer [Windows Controls]","NMTBGETINFOTIP","NMTBGETINFOTIP structure [Windows Controls]","NMTBGETINFOTIPA","NMTBGETINFOTIPW","_win32_NMTBGETINFOTIP","_win32_NMTBGETINFOTIP_cpp","commctrl/LPNMTBGETINFOTIP","commctrl/NMTBGETINFOTIP","commctrl/NMTBGETINFOTIPA","commctrl/NMTBGETINFOTIPW","controls.NMTBGETINFOTIP","controls._win32_NMTBGETINFOTIP"]
old-location: controls\NMTBGETINFOTIP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtbgetinfotip.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTBGETINFOTIPW, LPNMTBGETINFOTIP, LPNMTBGETINFOTIP structure pointer [Windows Controls], NMTBGETINFOTIP, NMTBGETINFOTIP structure [Windows Controls], NMTBGETINFOTIPA, NMTBGETINFOTIPW, _win32_NMTBGETINFOTIP, _win32_NMTBGETINFOTIP_cpp, commctrl/LPNMTBGETINFOTIP, commctrl/NMTBGETINFOTIP, commctrl/NMTBGETINFOTIPA, commctrl/NMTBGETINFOTIPW, controls.NMTBGETINFOTIP, controls._win32_NMTBGETINFOTIP'
f1_keywords:
- commctrl/NMTBGETINFOTIP
dev_langs:
- c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMTBGETINFOTIPW (Unicode) and NMTBGETINFOTIPA (ANSI)
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
- NMTBGETINFOTIP
- NMTBGETINFOTIPA
- NMTBGETINFOTIPW
targetos: Windows
req.typenames: NMTBGETINFOTIPW, *LPNMTBGETINFOTIPW
req.redist: 
ms.custom: 19H1
---

# NMTBGETINFOTIPW structure


## -description


Contains and receives infotip information for a toolbar item. This structure is used with the <a href="https://docs.microsoft.com/windows/desktop/Controls/tbn-getdispinfo">TBN_GETINFOTIP</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification. 


### -field pszText

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Address of a character buffer that receives the infotip text. 


### -field cchTextMax

Type: <b>int</b>

Size of the buffer, in characters, at 
					<b>pszText</b>. In most cases, the buffer will be INFOTIPSIZE characters in size, but you should always make sure that your application does not copy more than 
					<b>cchTextMax</b> characters to the buffer at 
					<b>pszText</b>. 


### -field iItem

Type: <b>int</b>

The command identifier of the item for which infotip information is being requested. This member is filled in by the control before sending the notification code. 


### -field lParam

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The application-defined value associated with the item for which infotip information is being requested. This member is filled in by the control before sending the notification code. 


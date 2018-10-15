---
UID: NS:commctrl.tagNMTBGETINFOTIPW
title: tagNMTBGETINFOTIPW
author: windows-sdk-content
description: Contains and receives infotip information for a toolbar item. This structure is used with the TBN_GETINFOTIP notification code.
old-location: controls\NMTBGETINFOTIP.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtbgetinfotip.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*LPNMTBGETINFOTIPW, LPNMTBGETINFOTIP, LPNMTBGETINFOTIP structure pointer [Windows Controls], NMTBGETINFOTIP, NMTBGETINFOTIP structure [Windows Controls], NMTBGETINFOTIPA, NMTBGETINFOTIPW, _win32_NMTBGETINFOTIP, _win32_NMTBGETINFOTIP_cpp, commctrl/LPNMTBGETINFOTIP, commctrl/NMTBGETINFOTIP, commctrl/NMTBGETINFOTIPA, commctrl/NMTBGETINFOTIPW, controls.NMTBGETINFOTIP, controls._win32_NMTBGETINFOTIP, tagNMTBGETINFOTIPW"
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
product: Windows
targetos: Windows
req.typenames: NMTBGETINFOTIPW, *LPNMTBGETINFOTIPW
req.redist: 
---

# tagNMTBGETINFOTIPW structure


## -description


Contains and receives infotip information for a toolbar item. This structure is used with the <a href="https://msdn.microsoft.com/ed6e4141-2bf8-4a92-8349-f3833c87fcf3">TBN_GETINFOTIP</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The application-defined value associated with the item for which infotip information is being requested. This member is filled in by the control before sending the notification code. 


---
UID: NS:commctrl.tagNMTVGETINFOTIPW
title: NMTVGETINFOTIPW
author: windows-sdk-content
description: Contains and receives tree-view item information needed to display a tooltip for an item. This structure is used with the TVN_GETINFOTIP notification code.
old-location: controls\NMTVGETINFOTIP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvgetinfotip.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNMTVGETINFOTIPW, LPNMTVGETINFOTIP, LPNMTVGETINFOTIP structure pointer [Windows Controls], NMTVGETINFOTIP, NMTVGETINFOTIP structure [Windows Controls], NMTVGETINFOTIPA, NMTVGETINFOTIPW, _win32_NMTVGETINFOTIP, _win32_NMTVGETINFOTIP_cpp, commctrl/LPNMTVGETINFOTIP, commctrl/NMTVGETINFOTIP, commctrl/NMTVGETINFOTIPA, commctrl/NMTVGETINFOTIPW, controls.NMTVGETINFOTIP, controls._win32_NMTVGETINFOTIP"
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMTVGETINFOTIPW (Unicode) and NMTVGETINFOTIPA (ANSI)
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
 - NMTVGETINFOTIP
 - NMTVGETINFOTIPA
 - NMTVGETINFOTIPW
product: Windows
targetos: Windows
req.typenames: NMTVGETINFOTIPW, *LPNMTVGETINFOTIPW
req.redist: 
---

# NMTVGETINFOTIPW structure


## -description


Contains and receives tree-view item information needed to display a tooltip for an item. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb773522(v=VS.85).aspx">TVN_GETINFOTIP</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about this notification. 


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Address of a character buffer that contains the text to be displayed. If you want to change the text displayed in the tooltip, you will need to modify the contents of this buffer. The size of this buffer is specified by the 
					<b>cchTextMax</b> structure. 


### -field cchTextMax

Type: <b>int</b>

Size of the buffer at 
					<b>pszText</b>, in characters. Although you should never assume that this buffer will be of any particular size, the INFOTIPSIZE value can be used for design purposes. 


### -field hItem

Type: <b>HTREEITEM</b>

Tree handle to the item for which the tooltip is being displayed. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Application-defined data associated with the item for which the tooltip is being displayed. 


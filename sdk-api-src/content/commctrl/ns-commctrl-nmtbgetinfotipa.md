---
UID: NS:commctrl.tagNMTBGETINFOTIPA
title: NMTBGETINFOTIPA (commctrl.h)
description: Contains and receives infotip information for a toolbar item. This structure is used with the TBN_GETINFOTIP notification code. (ANSI)
helpviewer_keywords: ["*LPNMTBGETINFOTIPA","LPNMTBGETINFOTIP","LPNMTBGETINFOTIP structure pointer [Windows Controls]","NMTBGETINFOTIP","NMTBGETINFOTIP structure [Windows Controls]","NMTBGETINFOTIPA","NMTBGETINFOTIPW","_win32_NMTBGETINFOTIP","_win32_NMTBGETINFOTIP_cpp","commctrl/LPNMTBGETINFOTIP","commctrl/NMTBGETINFOTIP","commctrl/NMTBGETINFOTIPA","commctrl/NMTBGETINFOTIPW","controls.NMTBGETINFOTIP","controls._win32_NMTBGETINFOTIP"]
old-location: controls\NMTBGETINFOTIP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtbgetinfotip.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTBGETINFOTIPA, LPNMTBGETINFOTIP, LPNMTBGETINFOTIP structure pointer [Windows Controls], NMTBGETINFOTIP, NMTBGETINFOTIP structure [Windows Controls], NMTBGETINFOTIPA, NMTBGETINFOTIPW, _win32_NMTBGETINFOTIP, _win32_NMTBGETINFOTIP_cpp, commctrl/LPNMTBGETINFOTIP, commctrl/NMTBGETINFOTIP, commctrl/NMTBGETINFOTIPA, commctrl/NMTBGETINFOTIPW, controls.NMTBGETINFOTIP, controls._win32_NMTBGETINFOTIP'
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
targetos: Windows
req.typenames: NMTBGETINFOTIPA, *LPNMTBGETINFOTIPA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMTBGETINFOTIPA
 - commctrl/tagNMTBGETINFOTIPA
 - LPNMTBGETINFOTIPA
 - commctrl/LPNMTBGETINFOTIPA
 - NMTBGETINFOTIPA
 - commctrl/NMTBGETINFOTIPA
dev_langs:
 - c++
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
---

# NMTBGETINFOTIPA structure


## -description

Contains and receives infotip information for a toolbar item. This structure is used with the <a href="/windows/desktop/Controls/tbn-getdispinfo">TBN_GETINFOTIP</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The application-defined value associated with the item for which infotip information is being requested. This member is filled in by the control before sending the notification code.

## -remarks

> [!NOTE]
> The commctrl.h header defines NMTBGETINFOTIP as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

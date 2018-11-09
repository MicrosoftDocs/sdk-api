---
UID: NS:commctrl.NMTBDISPINFOW
title: NMTBDISPINFOW
author: windows-sdk-content
description: Contains and receives display information for a toolbar item. This structure is used with the TBN_GETDISPINFO notification code.
old-location: controls\NMTBDISPINFO.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtbdispinfo.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPNMTBDISPINFOW, LPNMTBDISPINFO, LPNMTBDISPINFO structure pointer [Windows Controls], NMTBDISPINFO, NMTBDISPINFO structure [Windows Controls], NMTBDISPINFOA, NMTBDISPINFOW, TBNF_DI_SETITEM, TBNF_IMAGE, TBNF_TEXT, _win32_NMTBDISPINFO, _win32_NMTBDISPINFO_cpp, commctrl/LPNMTBDISPINFO, commctrl/NMTBDISPINFO, commctrl/NMTBDISPINFOA, commctrl/NMTBDISPINFOW, controls.NMTBDISPINFO, controls._win32_NMTBDISPINFO"
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
req.unicode-ansi: NMTBDISPINFOW (Unicode) and NMTBDISPINFOA (ANSI)
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
 - NMTBDISPINFO
 - NMTBDISPINFOA
 - NMTBDISPINFOW
product: Windows
targetos: Windows
req.typenames: NMTBDISPINFOW, *LPNMTBDISPINFOW
req.redist: 
---

# NMTBDISPINFOW structure


## -description


Contains and receives display information for a toolbar item. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb787268(v=VS.85).aspx">TBN_GETDISPINFO</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about the notification. 


### -field dwMask

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD</a></b>

Set of flags that indicate which members of this structure are being requested. This can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TBNF_IMAGE"></a><a id="tbnf_image"></a><dl>
<dt><b>TBNF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The item's image index is being requested. The image index must be placed in the 
						<b>iImage</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="TBNF_TEXT"></a><a id="tbnf_text"></a><dl>
<dt><b>TBNF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
Not currently implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="TBNF_DI_SETITEM"></a><a id="tbnf_di_setitem"></a><dl>
<dt><b>TBNF_DI_SETITEM</b></dt>
</dl>
</td>
<td width="60%">
Set this flag when processing <a href="https://msdn.microsoft.com/en-us/library/Bb787268(v=VS.85).aspx">TBN_GETDISPINFO</a>; the toolbar control will retain the supplied information and not request it again.

</td>
</tr>
</table>
 


### -field idCommand

Type: <b>int</b>

Command identifier of the item for which display information is being requested. This member is filled in by the control before it sends the notification code. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD_PTR</a></b>

Application-defined value associated with the item for which display information is being requested. This member is filled in by the control before sending the notification code. 


### -field iImage

Type: <b>int</b>

Image index for the item. 


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPTSTR</a></b>

Pointer to a character buffer that receives the item's text. 


### -field cchText

Type: <b>int</b>

Size of the 
					<b>pszText</b> buffer, in characters. 


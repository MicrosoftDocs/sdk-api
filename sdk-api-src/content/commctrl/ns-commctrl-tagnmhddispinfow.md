---
UID: NS:commctrl.tagNMHDDISPINFOW
title: tagNMHDDISPINFOW
author: windows-sdk-content
description: Contains information used in handling HDN_GETDISPINFO notification codes.
old-location: controls\NMHDDISPINFO.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\header\structures\nmhddispinfo.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*LPNMHDDISPINFOW, HDI_DI_SETITEM, HDI_IMAGE, HDI_LPARAM, HDI_TEXT, LPNMHDDISPINFO, LPNMHDDISPINFO structure pointer [Windows Controls], NMHDDISPINFO, NMHDDISPINFO structure [Windows Controls], NMHDDISPINFOA, NMHDDISPINFOW, _win32_NMHDDISPINFO, _win32_NMHDDISPINFO_cpp, commctrl/LPNMHDDISPINFO, commctrl/NMHDDISPINFO, commctrl/NMHDDISPINFOA, commctrl/NMHDDISPINFOW, controls.NMHDDISPINFO, controls._win32_NMHDDISPINFO, tagNMHDDISPINFOW"
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
req.unicode-ansi: NMHDDISPINFOW (Unicode) and NMHDDISPINFOA (ANSI)
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
 - NMHDDISPINFO
 - NMHDDISPINFOA
 - NMHDDISPINFOW
product: Windows
targetos: Windows
req.typenames: NMHDDISPINFOW, *LPNMHDDISPINFOW
req.redist: 
---

# tagNMHDDISPINFOW structure


## -description


Contains information used in handling <a href="https://msdn.microsoft.com/51522df0-83ae-4d9a-a8fc-31083e24242a">HDN_GETDISPINFO</a> notification codes. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure containing information about this notification code. 


### -field iItem

Type: <b>int</b>

The zero-based index of the item in the header control. 


### -field mask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A set of bit flags specifying which members of the structure must be filled in by the owner of the header control. This value can be a combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HDI_TEXT"></a><a id="hdi_text"></a><dl>
<dt><b>HDI_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>pszText</b> field must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="HDI_IMAGE"></a><a id="hdi_image"></a><dl>
<dt><b>HDI_IMAGE</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 4.70</a>. The 
						<b>iImage</b> field must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="HDI_LPARAM"></a><a id="hdi_lparam"></a><dl>
<dt><b>HDI_LPARAM</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>lParam</b> field must be filled in.

</td>
</tr>
<tr>
<td width="40%"><a id="HDI_DI_SETITEM"></a><a id="hdi_di_setitem"></a><dl>
<dt><b>HDI_DI_SETITEM</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 4.70</a>. A return value. Indicates that the header control should store the item information and not ask for it again.

</td>
</tr>
</table>
 


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to a null-terminated string containing the text that will be displayed for the header item. 


### -field cchTextMax

Type: <b>int</b>

The size of the buffer that 
					<b>pszText</b> points to. 


### -field iImage

Type: <b>int</b>

The zero-based index of an image within the image list. The specified image will be displayed with the header item, but it does not take the place of the item's bitmap. If 
					<b>iImage</b> is set to I_IMAGECALLBACK, the control requests image information for this item by using an <a href="https://msdn.microsoft.com/51522df0-83ae-4d9a-a8fc-31083e24242a">HDN_GETDISPINFO</a> notification code. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

An application-defined value to associate with the item. 


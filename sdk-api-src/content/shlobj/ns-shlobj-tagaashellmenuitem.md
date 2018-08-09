---
UID: NS:shlobj.tagAASHELLMENUITEM
title: tagAASHELLMENUITEM
author: windows-sdk-content
description: Contains information about a menu item.
old-location: shell\AASHELLMENUITEM_str.htm
old-project: shell
ms.assetid: 9d5ccbae-cc56-446f-be67-9623247d5045
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPAASHELLMENUITEM, AASHELLMENUITEM, AASHELLMENUITEM structure [Windows Shell], LPAASHELLMENUITEM, LPAASHELLMENUITEM structure pointer [Windows Shell], _win32_AASHELLMENUITEM_str, shell.AASHELLMENUITEM_str, shlobj/AASHELLMENUITEM, shlobj/LPAASHELLMENUITEM, tagAASHELLMENUITEM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj.h
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
req.typenames: AASHELLMENUITEM, *LPAASHELLMENUITEM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj.h
api_name:
 - AASHELLMENUITEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# tagAASHELLMENUITEM structure


## -description


Contains information about a menu item.


## -struct-fields




### -field lpReserved1

Type: <b>VOID</b>

Reserved. Applications should ignore this value.


### -field iReserved

Type: <b>int</b>

Reserved. Applications should ignore this value.


### -field uiReserved

Type: <b>UINT</b>

Reserved. Applications should ignore this value.


### -field lpName

Type: <b>LPAASHELLMENUFILENAME</b>

If the selected menu item represents a file, this member is a pointer to an <a href="https://msdn.microsoft.com/f84e837f-61b0-4df4-9ff7-dc2d3d898d99">AASHELLMENUFILENAME</a> structure that contains the name of the file. Otherwise this member is <b>NULL</b>.


### -field psz

Type: <b>LPTSTR</b>

A pointer to the string that contains the text to use if there is no file.


## -remarks



<div class="alert"><b>Important</b>  This structure cannot be used with operating systems later than Windows 2000.</div>
<div> </div>
If the menu belongs to the Windows Explorer process and the menu item is MFT_OWNERDRAW and <b>dwItemData</b> is not <b>NULL</b>, then the <b>dwItemData</b> member can be probed to determine whether it is a Windows Explorer menu that shows owner-drawn file names.

The accessibility tool might treat the <b>dwItemData</b> member as a pointer to an <b>AASHELLMENUITEM</b> structure in the process that owns the menu. In this case the <b>lpName</b> and <b>psz</b> members might be examined to determine the identity of the menu item. If <b>lpName</b> is not <b>NULL</b>, then the menu item represents a file name, expressed as an <a href="https://msdn.microsoft.com/f84e837f-61b0-4df4-9ff7-dc2d3d898d99">AASHELLMENUFILENAME</a> structure. If <b>lpName</b> is <b>NULL</b> but <b>psz</b> is not <b>NULL</b>, then the menu item represents a string that is pointed to by the <b>psz</b> member.

The <b>lpName</b> and <b>psz</b> members contain pointers into the process that owns the menu.

<div class="alert"><b>Note</b>  Not all owner-draw menus in the Windows Explorer process conform to this convention.</div>
<div> </div>
Applications that probe owner-draw menu data must validate all data read from the process.




## -see-also




<a href="https://msdn.microsoft.com/f84e837f-61b0-4df4-9ff7-dc2d3d898d99">AASHELLMENUFILENAME</a>
 

 


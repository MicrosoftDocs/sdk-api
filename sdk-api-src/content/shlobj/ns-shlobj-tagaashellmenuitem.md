---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


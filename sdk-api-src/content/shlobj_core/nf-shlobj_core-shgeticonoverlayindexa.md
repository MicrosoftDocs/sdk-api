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

# SHGetIconOverlayIndexA function


## -description


Returns the index of the overlay icon in the system image list.


## -parameters




### -param pszIconPath [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length <b>MAX_PATH</b> that contains the fully qualified path of the file that contains the icon.


### -param iIconIndex

Type: <b>int</b>

The icon's index in the file pointed to by <i>pszIconPath</i>. To request a standard overlay icon, set <i>pszIconPath</i> to <b>NULL</b>, and <i>iIconIndex</i> to one of the following:



#### IDO_SHGIOI_SHARE (0x0FFFFFFF)

The overlay icon that indicates a shared folder.



#### IDO_SHGIOI_LINK (0x0FFFFFFE)

The overlay icon that indicates a linked folder or file.



#### IDO_SHGIOI_SLOWFILE (0x0FFFFFFD)

The overlay icon that indicates a slow file.



#### IDO_SHGIOI_DEFAULT (0x0FFFFFFC)

<b>Windows 7 and later</b>. The overlay icon that indicates that the item is the default in a set. One example is the default printer.


## -returns



Type: <b>int</b>

Returns the index of the overlay icon in the system image list if successful, or -1 otherwise.




## -remarks



Icon overlays are part of the system image list. They have two identifiers. The first is a one-based overlay index that identifies the overlay relative to other overlays in the image list. The other is an image index that identifies the actual image. These two indexes are equivalent to the values that you assign to the <i>iOverlay</i> and <i>iImage</i> parameters, respectively, when you add an icon overlay to a private image list with <a href="https://msdn.microsoft.com/8cb1babc-01bd-4aae-9bc7-073050242ce4">ImageList_SetOverlayImage</a>. <b>SHGetIconOverlayIndex</b> returns the overlay index. To convert an overlay index to its equivalent image index, call <a href="https://msdn.microsoft.com/6619d390-0c23-41ff-a07b-31425e47712b">INDEXTOOVERLAYMASK</a>.

<div class="alert"><b>Note</b>  After the image has been loaded into the system image list during initialization, it cannot be changed. The file name and index specified by <i>pszIconPath</i> and <i>iIconIndex</i> are used only to identify the icon overlay. <b>SHGetIconOverlayIndex</b> cannot be used to modify the system image list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1a1d03ca-0922-41df-8cec-e74a16ed3bd6">IShellIconOverlay</a>



<a href="https://msdn.microsoft.com/c093bc13-def7-411d-b741-50996ffad84b">IShellIconOverlayIdentifier</a>
 

 


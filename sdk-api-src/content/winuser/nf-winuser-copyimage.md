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

# CopyImage function


## -description


Creates a new image (icon, cursor, or bitmap) and copies the attributes of the specified image to the new one. If necessary, the function stretches the bits to fit the desired size of the new image.


## -parameters




### -param h

TBD


### -param type

TBD


### -param cx

TBD


### -param cy

TBD


### -param flags

TBD




#### - cxDesired [in]

Type: <b>int</b>

The desired width, in pixels, of the image. If this is zero, then the returned image will have the same width as the original <i>hImage</i>. 


#### - cyDesired [in]

Type: <b>int</b>

The desired height, in pixels, of the image. If this is zero, then the returned image will have the same height as the original <i>hImage</i>. 


#### - fuFlags [in]

Type: <b>UINT</b>

This parameter can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LR_COPYDELETEORG"></a><a id="lr_copydeleteorg"></a><dl>
<dt><b>LR_COPYDELETEORG</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Deletes the original image after creating the copy.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_COPYFROMRESOURCE"></a><a id="lr_copyfromresource"></a><dl>
<dt><b>LR_COPYFROMRESOURCE</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Tries to reload an icon or cursor resource from the original resource file rather than simply copying the current image. This is useful for creating a different-sized copy when the resource file contains multiple sizes of the resource. Without this flag, <b>CopyImage</b> stretches the original image to the new size. If this flag is set, <b>CopyImage</b> uses the size in the resource file closest to the desired size. This will succeed only if <i>hImage</i> was loaded by <a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a> or <a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>, or by <a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a> with the LR_SHARED flag.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_COPYRETURNORG"></a><a id="lr_copyreturnorg"></a><dl>
<dt><b>LR_COPYRETURNORG</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Returns the original <i>hImage</i> if it satisfies the criteria for the copy—that is, correct dimensions and color depth—in which case the <b>LR_COPYDELETEORG</b> flag is ignored. If this flag is not specified, a new object is always created.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_CREATEDIBSECTION"></a><a id="lr_createdibsection"></a><dl>
<dt><b>LR_CREATEDIBSECTION</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
If this is set and a new bitmap is created, the bitmap is created as a DIB section. Otherwise, the bitmap image is created as a device-dependent bitmap. This flag is only valid if <i>uType</i> is <b>IMAGE_BITMAP</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_DEFAULTSIZE"></a><a id="lr_defaultsize"></a><dl>
<dt><b>LR_DEFAULTSIZE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Uses the width or height specified by the system metric values for cursors or icons, if the <i>cxDesired</i> or <i>cyDesired</i> values are set to zero. If this flag is not specified and <i>cxDesired</i> and <i>cyDesired</i> are set to zero, the function uses the actual resource size. If the resource contains multiple images, the function uses the size of the first image.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_MONOCHROME"></a><a id="lr_monochrome"></a><dl>
<dt><b>LR_MONOCHROME</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Creates a new monochrome image. 

</td>
</tr>
</table>
 


#### - hImage [in]

Type: <b>HANDLE</b>

A handle to the image to be copied. 


#### - uType [in]

Type: <b>UINT</b>

The type of image to be copied. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_BITMAP"></a><a id="image_bitmap"></a><dl>
<dt><b>IMAGE_BITMAP</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Copies a bitmap.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_CURSOR"></a><a id="image_cursor"></a><dl>
<dt><b>IMAGE_CURSOR</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Copies a cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_ICON"></a><a id="image_icon"></a><dl>
<dt><b>IMAGE_ICON</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Copies an icon.

</td>
</tr>
</table>
 


## -returns



Type: <b>HANDLE</b>

If the function succeeds, the return value is the handle to the newly created image.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



When you are finished using the resource, you can release its associated memory by calling one of the functions in the following table. 

<table class="clsStd">
<tr>
<th>Resource</th>
<th>Release function</th>
</tr>
<tr>
<td>Bitmap</td>
<td>
<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>
</td>
</tr>
<tr>
<td>Cursor</td>
<td>
<a href="https://msdn.microsoft.com/fee6d837-9fc7-4ea6-b5d7-3889a64ccdea">DestroyCursor</a>
</td>
</tr>
<tr>
<td>Icon</td>
<td>
<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>
</td>
</tr>
</table>
 

The system automatically deletes the resource when its process terminates, however, calling the appropriate function saves memory and decreases the size of the process's working set. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 


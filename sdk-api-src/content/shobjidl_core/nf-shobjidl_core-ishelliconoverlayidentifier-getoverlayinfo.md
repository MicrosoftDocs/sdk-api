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

# IShellIconOverlayIdentifier::GetOverlayInfo


## -description


Provides the location of the icon overlay's bitmap.


## -parameters




### -param pwszIconFile [out]

Type: <b>PWSTR</b>

A null-terminated Unicode string that contains the fully qualified path of the file containing the icon. The .dll, .exe, and .ico file types are all acceptable. You must set the <b>ISIOI_ICONFILE</b> flag in <i>pdwFlags</i> if you return a file name.


### -param cchMax

Type: <b>int</b>

The size of the <i>pwszIconFile</i> buffer, in Unicode characters.


### -param pIndex [out]

Type: <b>int*</b>

Pointer to an index value used to identify the icon in a file that contains multiple icons. You must set the <b>ISIOI_ICONINDEX</b> flag in <i>pdwFlags</i> if you return an index.


### -param pdwFlags [out]

Type: <b>DWORD*</b>

Pointer to a bitmap that specifies the information that is being returned by the method. This parameter can be one or both of the following values.



#### ISIOI_ICONFILE (0x00000001)

The path of the icon file is returned through <i>pwszIconFile</i>.



#### ISIOI_ICONINDEX (0x00000002)

There is more than one icon in <i>pwszIconFile</i>. The icon's index is returned through <i>pIndex</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by the Shell at startup so that the handler's icon overlay can be added to the system image list. After initialization is complete, the Shell calls <b>GetOverlayInfo</b> when it needs to display the handler's icon overlay.

<div class="alert"><b>Note</b>  Once the image has been loaded into the system image list during initialization, it cannot be changed. After initialization, the file name and index are used only to identify the icon overlay. The system will not load a new icon overlay. When <b>GetOverlayInfo</b> is called, your handler must return the same file name and index that were specified when the function was first called.</div>
<div> </div>



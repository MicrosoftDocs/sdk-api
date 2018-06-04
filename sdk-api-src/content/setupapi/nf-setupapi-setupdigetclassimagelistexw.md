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

# SetupDiGetClassImageListExW function


## -description


The <b>SetupDiGetClassImageListEx</b> function builds an image list of bitmaps for every class installed on a local or remote system.


## -parameters




### -param ClassImageListData [out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552339">SP_CLASSIMAGELIST_DATA</a> structure to receive information regarding the class image list, including a handle to the image list. The <b>cbSize</b> field of this structure must be initialized with the size of the structure, in bytes, before calling this function or it will fail.


### -param MachineName [in, optional]

A pointer to NULL-terminated string that supplies the name of a remote system for whose classes <b>SetupDiGetClassImageListEx must build </b>the bitmap. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, <b>SetupDiGetClassImageListEx</b> builds the list for the local system.


### -param Reserved

Must be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The image list built by this function should be destroyed by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff550995">SetupDiDestroyClassImageList</a>.

<div class="alert"><b>Note</b>    Class-specific icons on a remote computer can only be displayed if the class is also present on the local computer. Thus, if the remote computer has class <i>X</i>, but class <i>X</i> is not installed locally, then the generic (unknown) icon will be returned.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550995">SetupDiDestroyClassImageList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551080">SetupDiGetClassImageList</a>
 

 


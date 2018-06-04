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

# ImageList_Copy function


## -description


Copies images within a given image list. 


## -parameters




### -param himlDst

Type: <b>HIMAGELIST</b>

A handle to an image list that is the target of the copy operation. In current versions of Windows, both <i>himlDst</i> and <i>himlSrc</i> must be identical. 


### -param iDst

Type: <b>int</b>

The zero-based index of the image to be used as the destination of the copy operation. 


### -param himlSrc

Type: <b>HIMAGELIST</b>

A handle to an image list that is the target of the copy operation. In current versions of Windows, both <i>himlDst</i> and <i>himlSrc</i> must be identical. 


### -param iSrc

Type: <b>int</b>

The zero-based index of the image to be used as the source of the copy operation. 


### -param uFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

the bit flag value that specifies the type of copy operation to be made. This parameter can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILCF_MOVE"></a><a id="ilcf_move"></a><dl>
<dt><b>ILCF_MOVE</b></dt>
</dl>
</td>
<td width="60%">
The source image is copied to the destination image's index. This operation results in multiple instances of a given image.

</td>
</tr>
<tr>
<td width="40%"><a id="ILCF_SWAP"></a><a id="ilcf_swap"></a><dl>
<dt><b>ILCF_SWAP</b></dt>
</dl>
</td>
<td width="60%">
The source and destination images exchange positions within the image list.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 




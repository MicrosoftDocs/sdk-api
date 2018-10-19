---
UID: NF:shimgdata.IShellImageData.IsEditable
title: IShellImageData::IsEditable
author: windows-sdk-content
description: Determines whether the image can be edited.
old-location: shell\IShellImageData_IsEditable.htm
tech.root: shell
ms.assetid: 81dbb486-0b35-44ff-9aa2-2e449995591e
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IShellImageData interface [Windows Shell],IsEditable method, IShellImageData.IsEditable, IShellImageData::IsEditable, IsEditable, IsEditable method [Windows Shell], IsEditable method [Windows Shell],IShellImageData interface, _shell_IShellImageData_IsEditable, shell.IShellImageData_IsEditable, shimgdata/IShellImageData::IsEditable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData.IsEditable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageData::IsEditable


## -description


Determines whether the image can be edited.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The image can be edited.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The image cannot be edited, the image has not been decoded, or the decoding process failed.

</td>
</tr>
</table>
 




## -remarks



At this time, the criteria for determining whether the image can be edited is solely that it is a Tagged Image File Format (TIFF) image with the Exif IFD tag set.




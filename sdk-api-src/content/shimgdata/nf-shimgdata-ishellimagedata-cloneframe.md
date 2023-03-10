---
UID: NF:shimgdata.IShellImageData.CloneFrame
title: IShellImageData::CloneFrame (shimgdata.h)
description: Retrieves a clone of the current image or frame.
helpviewer_keywords: ["CloneFrame","CloneFrame method [Windows Shell]","CloneFrame method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","CloneFrame method","IShellImageData.CloneFrame","IShellImageData::CloneFrame","_shell_IShellImageData_CloneFrame","shell.IShellImageData_CloneFrame","shimgdata/IShellImageData::CloneFrame"]
old-location: shell\IShellImageData_CloneFrame.htm
tech.root: shell
ms.assetid: 220d307a-7969-443c-963b-80132509ad8b
ms.date: 12/05/2018
ms.keywords: CloneFrame, CloneFrame method [Windows Shell], CloneFrame method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],CloneFrame method, IShellImageData.CloneFrame, IShellImageData::CloneFrame, _shell_IShellImageData_CloneFrame, shell.IShellImageData_CloneFrame, shimgdata/IShellImageData::CloneFrame
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellImageData::CloneFrame
 - shimgdata/IShellImageData::CloneFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData.CloneFrame
---

# IShellImageData::CloneFrame


## -description

Retrieves a clone of the current image or frame.

## -parameters

### -param ppImg [in, out]

Type: <b>Image**</b>

The address that receives a pointer to the clone image. If this parameter is <b>NULL</b> on entry, an unhandled exception results.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppImg</i> parameter is <b>NULL</b> on entry or the image cannot be cloned. In the latter case, <i>ppImg</i> is set to <b>NULL</b>.
          

</td>
</tr>
</table>

## -remarks

In the case of a multiframed image such as a .gif file, the current frame is cloned. In the case of non-multiframed images such a .jpg file, the entire image is cloned.


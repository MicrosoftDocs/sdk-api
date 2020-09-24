---
UID: NF:shimgdata.IShellImageData.Scale
title: IShellImageData::Scale (shimgdata.h)
description: Adjusts the size of an image.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","Scale method","IShellImageData.Scale","IShellImageData::Scale","Scale","Scale method [Windows Shell]","Scale method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_Scale","shell.IShellImageData_Scale","shimgdata/IShellImageData::Scale"]
old-location: shell\IShellImageData_Scale.htm
tech.root: shell
ms.assetid: ebcc9cc1-b6ee-4fb9-9125-54d6a9ee9434
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],Scale method, IShellImageData.Scale, IShellImageData::Scale, Scale, Scale method [Windows Shell], Scale method [Windows Shell],IShellImageData interface, _shell_IShellImageData_Scale, shell.IShellImageData_Scale, shimgdata/IShellImageData::Scale
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
 - IShellImageData::Scale
 - shimgdata/IShellImageData::Scale
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
 - IShellImageData.Scale
---

# IShellImageData::Scale


## -description

Adjusts the size of an image.

## -parameters

### -param cx [in]

Type: <b>ULONG</b>

The horizontal (x) dimension. If this value is 0, the x dimension is set to a scaled value based on the point specified in <i>cy</i>.

### -param cy [in]

Type: <b>ULONG</b>

The vertical (y) dimension. If this value is 0, the y dimension is set to a scaled value based on the point specified in <i>cx</i>.

### -param hints [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-interpolationmode">InterpolationMode</a></b>

A member of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-interpolationmode">InterpolationMode</a> enumeration, specifying the algorithm that is used when the image is scaled.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful or an error value otherwise, including the following:

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
The image was not previously decoded or the call to <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-decode">IShellImageData::Decode</a> failed. Other internal calls also can cause this error to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTVALIDFORANIMATEDIMAGE</b></dt>
</dl>
</td>
<td width="60%">
The image is an animated image and cannot be scaled using this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The internal object cannot be instantiated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The process was stopped by the calling application through a registered instance of <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedataabort">IShellImageDataAbort</a>.

</td>
</tr>
</table>
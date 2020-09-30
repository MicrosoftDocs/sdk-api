---
UID: NF:shimgdata.IShellImageData.Draw
title: IShellImageData::Draw (shimgdata.h)
description: Draws a decoded image.
helpviewer_keywords: ["Draw","Draw method [Windows Shell]","Draw method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","Draw method","IShellImageData.Draw","IShellImageData::Draw","_shell_IShellImageData_Draw","shell.IShellImageData_Draw","shimgdata/IShellImageData::Draw"]
old-location: shell\IShellImageData_Draw.htm
tech.root: shell
ms.assetid: 35989c3b-15b9-4503-a883-99df730b2a80
ms.date: 12/05/2018
ms.keywords: Draw, Draw method [Windows Shell], Draw method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],Draw method, IShellImageData.Draw, IShellImageData::Draw, _shell_IShellImageData_Draw, shell.IShellImageData_Draw, shimgdata/IShellImageData::Draw
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
 - IShellImageData::Draw
 - shimgdata/IShellImageData::Draw
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
 - IShellImageData.Draw
---

# IShellImageData::Draw


## -description

Draws a decoded image.

## -parameters

### -param hdc [in]

Type: <b>HDC</b>

The handle of the image.

### -param prcDest [in]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>, measured in pixels, that specifies the bounds of the rendered image. The portion of the image specified by <i>prcSrc</i> is scaled to fill the rectangle specified by <i>prcDest</i>.

### -param prcSrc [in]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> that specifies the portion of the image to be drawn.

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
The image was not previously decoded, the call to <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-decode">IShellImageData::Decode</a> failed, or <i>hdc</i> is <b>NULL</b>. Other internal calls also can cause this error to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>prcDest</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The process was terminated by the calling application through a registered instance of <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedataabort">IShellImageDataAbort</a>.

</td>
</tr>
</table>

## -remarks

If <i>prcSrc</i> is <b>NULL</b>, nothing is drawn and the method returns S_OK.
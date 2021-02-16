---
UID: NF:shimgdata.IShellImageData.Decode
title: IShellImageData::Decode (shimgdata.h)
description: Decodes the image file, setting state.
helpviewer_keywords: ["Decode","Decode method [Windows Shell]","Decode method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","Decode method","IShellImageData.Decode","IShellImageData::Decode","SHIMGDEC_DEFAULT","SHIMGDEC_LOADFULL","SHIMGDEC_THUMBNAIL","_shell_IShellImageData_Decode","shell.IShellImageData_Decode","shimgdata/IShellImageData::Decode"]
old-location: shell\IShellImageData_Decode.htm
tech.root: shell
ms.assetid: 954424d6-cb90-46c1-a850-4e1113dfe2e4
ms.date: 12/05/2018
ms.keywords: Decode, Decode method [Windows Shell], Decode method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],Decode method, IShellImageData.Decode, IShellImageData::Decode, SHIMGDEC_DEFAULT, SHIMGDEC_LOADFULL, SHIMGDEC_THUMBNAIL, _shell_IShellImageData_Decode, shell.IShellImageData_Decode, shimgdata/IShellImageData::Decode
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
 - IShellImageData::Decode
 - shimgdata/IShellImageData::Decode
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
 - IShellImageData.Decode
---

# IShellImageData::Decode


## -description

Decodes the image file, setting state.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

One of the following flags.



#### SHIMGDEC_DEFAULT (0x00)

Create a full image.



#### SHIMGDEC_THUMBNAIL (0x01)

Decode only the thumbnail image.



#### SHIMGDEC_LOADFULL (0x02)

Load the entire image file into memory.

### -param cxDesired [in]

Type: <b>ULONG</b>

The desired horizontal size of the decoded image. This parameter is only used if the <b>SHIMGDEC_THUMBNAIL</b> flag is set. If the <b>SHIMGDEC_DEFAULT</b> flag is set instead, this value is ignored.

### -param cyDesired [in]

Type: <b>ULONG</b>

The desired vertical size of the decoded image. This parameter is only used if the <b>SHIMGDEC_THUMBNAIL</b> flag is set. If the <b>SHIMGDEC_DEFAULT</b> flag is set instead, this value is ignored.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

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
The file could not be loaded or the calling application stopped the decode process through a call to a registered <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedataabort">IShellImageDataAbort</a> (see <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-registerabort">IShellImageData::RegisterAbort</a> for more information).

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The path used to create this instance of <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> was a URL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The image has already been decoded.

</td>
</tr>
</table>

## -remarks

<b>IShellImageData::Decode</b> must be called prior to calling most <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> methods. Not doing so causes those methods to fail.

<b>IShellImageData::Decode</b> attempts to maintain the aspect ratio of the original image, so one of the values passed in <i>cxDesired</i> or <i>cyDesired</i> might be overridden to do so.
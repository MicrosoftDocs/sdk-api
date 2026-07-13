---
UID: NS:vfw.COMPVARS
title: COMPVARS (vfw.h)
description: The COMPVARS structure describes compressor settings for functions such as ICCompressorChoose, ICSeqCompressFrame, and ICCompressorFree.
helpviewer_keywords: ["*PCOMPVARS","COMPVARS","COMPVARS structure [Windows Multimedia]","ICMF_COMPVARS_VALID","_win32_COMPVARS_str","multimedia.compvars","vfw/COMPVARS"]
old-location: multimedia\compvars.htm
tech.root: Multimedia
ms.assetid: b34378cb-ccf0-4d97-a952-1966999e3f65
ms.date: 12/05/2018
ms.keywords: '*PCOMPVARS, COMPVARS, COMPVARS structure [Windows Multimedia], ICMF_COMPVARS_VALID, _win32_COMPVARS_str, multimedia.compvars, vfw/COMPVARS'
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COMPVARS, *PCOMPVARS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PCOMPVARS
 - vfw/PCOMPVARS
 - COMPVARS
 - vfw/COMPVARS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - COMPVARS
---

# COMPVARS structure


## -description

The <b>COMPVARS</b> structure describes compressor settings for functions such as <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a>, <a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframe">ICSeqCompressFrame</a>, and <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorfree">ICCompressorFree</a>.

## -struct-fields

### -field cbSize

Size, in bytes, of this structure. This member must be set to validate the structure before calling any function using this structure.

### -field dwFlags

Applicable flags. The following value is defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="ICMF_COMPVARS_VALID"></a><a id="icmf_compvars_valid"></a><dl>
<dt><b>ICMF_COMPVARS_VALID</b></dt>
</dl>
</td>
<td width="60%">
Data in this structure is valid and has been manually entered. Set this flag before you call any function if you fill this structure manually. Do not set this flag if you let <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a> initialize this structure.

</td>
</tr>
</table>

### -field hic

Handle to the compressor to use. You can open a compressor and obtain a handle of it by using the <a href="/windows/desktop/api/vfw/nf-vfw-icopen">ICOpen</a> function. You can also choose a compressor by using <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a>. <b>ICCompressorChoose</b> opens the chosen compressor and returns the handle of the compressor in this member. You can close the compressor by using <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorfree">ICCompressorFree</a>.

### -field fccType

Type of compressor used. Currently only <b>ICTYPE_VIDEO</b> (VIDC) is supported. This member can be set to zero.

### -field fccHandler

Four-character code of the compressor. Specify <b>NULL</b> to indicate the data is not to be recompressed. Specify "DIB" to indicate the data is an uncompressed, full frame. You can use this member to specify which compressor is selected by default when the dialog box is displayed.

### -field lpbiIn

Reserved; do not use.

### -field lpbiOut

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the image output format. You can specify a specific format to use or you can specify <b>NULL</b> to use the default compressor associated with the input format. You can also set the image output format by using <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a>.

### -field lpBitsOut

Reserved; do not use.

### -field lpBitsPrev

Reserved; do not use.

### -field lFrame

Reserved; do not use.

### -field lKey

Key-frame rate. Specify an integer to indicate the frequency that key frames are to occur in the compressed sequence or zero to not use key frames. You can also let <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a> set the key-frame rate selected in the dialog box. The <a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframestart">ICSeqCompressFrameStart</a> function uses the value of this member for making key frames.

### -field lDataRate

Data rate, in kilobytes per second. <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a> copies the selected data rate from the dialog box to this member.

### -field lQ

Quality setting. Specify a quality setting of 1 to 10,000 or specify<b> ICQUALITY_DEFAULT</b> to use the default quality setting. You can also let <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a> set the quality value selected in the dialog box. <a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframestart">ICSeqCompressFrameStart</a> uses the value of this member as its quality setting.

### -field lKeyCount

Reserved; do not use.

### -field lpState

Reserved; do not use.

### -field cbState

Reserved; do not use.

## -remarks

You can let <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a> fill the contents of this structure or you can do it manually. If you manually fill the structure, you must provide information for the following members: <b>cbSize</b>, <b>hic</b>, <b>lpbiOut</b>, <b>lKey</b>, and <b>lQ</b>. Also, you must set the <b>ICMF_COMPVARS_VALID</b> flag in the <b>dwFlags</b> member.

## -see-also

<a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a>



<a href="/windows/desktop/api/vfw/nf-vfw-iccompressorfree">ICCompressorFree</a>



<a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframe">ICSeqCompressFrame</a>



<a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframestart">ICSeqCompressFrameStart</a>



Video Compression Manager



<a href="/windows/desktop/Multimedia/video-compression-structures">Video Compression Structures</a>


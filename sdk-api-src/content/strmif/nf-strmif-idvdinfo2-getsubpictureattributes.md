---
UID: NF:strmif.IDvdInfo2.GetSubpictureAttributes
title: IDvdInfo2::GetSubpictureAttributes (strmif.h)
description: The GetSubpictureAttributes method retrieves the attributes of the specified subpicture stream in the specified title or menu.
helpviewer_keywords: ["GetSubpictureAttributes","GetSubpictureAttributes method [DirectShow]","GetSubpictureAttributes method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetSubpictureAttributes method","IDvdInfo2.GetSubpictureAttributes","IDvdInfo2::GetSubpictureAttributes","IDvdInfo2GetSubpictureAttributes","dshow.idvdinfo2_getsubpictureattributes","strmif/IDvdInfo2::GetSubpictureAttributes"]
old-location: dshow\idvdinfo2_getsubpictureattributes.htm
tech.root: dshow
ms.assetid: 3dce0c01-1d39-4f49-984b-8cce08a2e67b
ms.date: 4/26/2023
ms.keywords: GetSubpictureAttributes, GetSubpictureAttributes method [DirectShow], GetSubpictureAttributes method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetSubpictureAttributes method, IDvdInfo2.GetSubpictureAttributes, IDvdInfo2::GetSubpictureAttributes, IDvdInfo2GetSubpictureAttributes, dshow.idvdinfo2_getsubpictureattributes, strmif/IDvdInfo2::GetSubpictureAttributes
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo2::GetSubpictureAttributes
 - strmif/IDvdInfo2::GetSubpictureAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetSubpictureAttributes
---

# IDvdInfo2::GetSubpictureAttributes


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetSubpictureAttributes</code> method retrieves the attributes of the specified subpicture stream in the specified title or menu.

## -parameters

### -param ulStream [in]

Index number, from 0 through 31, of the subpicture stream to query. See Remarks.

### -param pATR [out]

Pointer to a [DVD_SubpictureAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_subpictureattributes) structure that receives the subpicture attributes.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No subpicture streams were found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
The subpicture has no defined attributes.

</td>
</tr>
</table>

## -remarks

The index numbers 0-31 are valid only for titles. Menus have only one subpicture stream, which must be specified using one of the constants in the table below:

<table>
<tr>
<th>Value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>DVD_STREAM_DATA_CURRENT (0x800)</td>
<td>To query the currently selected subpicture stream.</td>
</tr>
<tr>
<td>DVD_STREAM_DATA_VMGM (0x400)</td>
<td>To query the subpicture attributes for the Video Manager or "Top" Menu.</td>
</tr>
<tr>
<td>DVD_STREAM_DATA_VTSM (0x401)</td>
<td>To query the subpicture attributes for the currently selected Video Title Set Menu.</td>
</tr>
</table>
 

This method is demonstrated in the DVDSample application in <b>CDvdCore::GetSPAttributes()</b> and <b>CSPLangDlg::GetSPLang</b>.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-menus">Working With DVD Menus</a>
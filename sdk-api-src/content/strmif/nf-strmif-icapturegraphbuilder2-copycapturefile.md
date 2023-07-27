---
UID: NF:strmif.ICaptureGraphBuilder2.CopyCaptureFile
title: ICaptureGraphBuilder2::CopyCaptureFile (strmif.h)
description: The CopyCaptureFile method copies the valid media data from a capture file.
helpviewer_keywords: ["CopyCaptureFile","CopyCaptureFile method [DirectShow]","CopyCaptureFile method [DirectShow]","ICaptureGraphBuilder2 interface","ICaptureGraphBuilder2 interface [DirectShow]","CopyCaptureFile method","ICaptureGraphBuilder2.CopyCaptureFile","ICaptureGraphBuilder2::CopyCaptureFile","ICaptureGraphBuilder2CopyCaptureFile","dshow.icapturegraphbuilder2_copycapturefile","strmif/ICaptureGraphBuilder2::CopyCaptureFile"]
old-location: dshow\icapturegraphbuilder2_copycapturefile.htm
tech.root: dshow
ms.assetid: d4084b12-b082-45c2-9f07-625b980c7e4c
ms.date: 4/26/2023
ms.keywords: CopyCaptureFile, CopyCaptureFile method [DirectShow], CopyCaptureFile method [DirectShow],ICaptureGraphBuilder2 interface, ICaptureGraphBuilder2 interface [DirectShow],CopyCaptureFile method, ICaptureGraphBuilder2.CopyCaptureFile, ICaptureGraphBuilder2::CopyCaptureFile, ICaptureGraphBuilder2CopyCaptureFile, dshow.icapturegraphbuilder2_copycapturefile, strmif/ICaptureGraphBuilder2::CopyCaptureFile
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICaptureGraphBuilder2::CopyCaptureFile
 - strmif/ICaptureGraphBuilder2::CopyCaptureFile
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
 - ICaptureGraphBuilder2.CopyCaptureFile
---

# ICaptureGraphBuilder2::CopyCaptureFile


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>CopyCaptureFile</code> method copies the valid media data from a capture file.

## -parameters

### -param lpwstrOld [in]

Pointer to a wide-character string that contains the source file name.

### -param lpwstrNew [in]

Pointer to a wide-character string that contains the destination file name. Valid data is copied to this file.

### -param fAllowEscAbort [in]

Boolean value that specifies whether pressing the ESC key cancels the copy operation. If the value is <b>TRUE</b> and the user presses the ESC key, the operation halts. If the value is <b>FALSE</b>, the method ignores the ESC key.

### -param pCallback [in]

Pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-iamcopycapturefileprogress">IAMCopyCaptureFileProgress</a> interface to display progress information, or <b>NULL</b>. See Remarks for more information.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
User canceled the operation before it completed.

</td>
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
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Could not open the source file or destination file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -remarks

Typically, you will first capture to a large preallocated file. This method copies just the valid data to a new file. As a result, the new file can be much smaller than the original file.

The source and destination files must be AVI files. Other file types are not supported.

To display the progress of the copy operation, implement the <a href="/windows/desktop/api/strmif/nn-strmif-iamcopycapturefileprogress">IAMCopyCaptureFileProgress</a> interface and pass a pointer to the interface in the <i>pCallback</i> parameter. If <i>pCallback</i> is non-<b>NULL</b>, this method periodically calls the <a href="/windows/desktop/api/strmif/nf-strmif-iamcopycapturefileprogress-progress">IAMCopyCaptureFileProgress::Progress</a> method with an integer between 0 and 100 that specifies the percentage complete.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2 Interface</a>
---
UID: NF:strmif.IVMRImagePresenterExclModeConfig.SetXlcModeDDObjAndPrimarySurface
title: IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface (strmif.h)
description: The SetXlcModeDDObjAndPrimarySurface method informs the VMR of the DirectDraw object and primary surface that were created by the application.
helpviewer_keywords: ["IVMRImagePresenterExclModeConfig interface [DirectShow]","SetXlcModeDDObjAndPrimarySurface method","IVMRImagePresenterExclModeConfig.SetXlcModeDDObjAndPrimarySurface","IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface","SetXlcModeDDObjAndPrimarySurface","SetXlcModeDDObjAndPrimarySurface method [DirectShow]","SetXlcModeDDObjAndPrimarySurface method [DirectShow]","IVMRImagePresenterExclModeConfig interface","dshow.ivmrimagepresenterexclmodeconfig_setxlcmodeddobjandprimarysurface","strmif/IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface"]
old-location: dshow\ivmrimagepresenterexclmodeconfig_setxlcmodeddobjandprimarysurface.htm
tech.root: dshow
ms.assetid: 3af69975-fe3c-45e6-b1f5-ce2dbda9a4dc
ms.date: 4/26/2023
ms.keywords: IVMRImagePresenterExclModeConfig interface [DirectShow],SetXlcModeDDObjAndPrimarySurface method, IVMRImagePresenterExclModeConfig.SetXlcModeDDObjAndPrimarySurface, IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface, SetXlcModeDDObjAndPrimarySurface, SetXlcModeDDObjAndPrimarySurface method [DirectShow], SetXlcModeDDObjAndPrimarySurface method [DirectShow],IVMRImagePresenterExclModeConfig interface, dshow.ivmrimagepresenterexclmodeconfig_setxlcmodeddobjandprimarysurface, strmif/IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface
 - strmif/IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface
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
 - IVMRImagePresenterExclModeConfig.SetXlcModeDDObjAndPrimarySurface
---

# IVMRImagePresenterExclModeConfig::SetXlcModeDDObjAndPrimarySurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetXlcModeDDObjAndPrimarySurface</code> method informs the VMR of the DirectDraw object and primary surface that were created by the application.

## -parameters

### -param lpDDObj [in]

Specifies the Exclusive Mode DirectDraw object created by the application.

### -param lpPrimarySurf [in]

Specifies the primary surface associated with the DirectDraw object.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

The procedure for configuring and using an application-defined DirectDraw Exclusive Mode object is described in <a href="/windows/desktop/DirectShow/directdraw-exclusive-mode">DirectDraw Exclusive Mode</a>.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterexclmodeconfig">IVMRImagePresenterExclModeConfig Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrimagepresenterexclmodeconfig-getxlcmodeddobjandprimarysurface">IVMRImagePresenterExclModeConfig::GetXlcModeDDObjAndPrimarySurface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
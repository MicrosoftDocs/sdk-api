---
UID: NF:strmif.IVMRWindowlessControl.DisplayModeChanged
title: IVMRWindowlessControl::DisplayModeChanged (strmif.h)
description: The DisplayModeChanged method informs the VMR that a WM_DISPLAYCHANGE message has been received by the application.
helpviewer_keywords: ["DisplayModeChanged","DisplayModeChanged method [DirectShow]","DisplayModeChanged method [DirectShow]","IVMRWindowlessControl interface","IVMRWindowlessControl interface [DirectShow]","DisplayModeChanged method","IVMRWindowlessControl.DisplayModeChanged","IVMRWindowlessControl::DisplayModeChanged","IVMRWindowlessControlDisplayModeChanged","dshow.ivmrwindowlesscontrol_displaymodechanged","strmif/IVMRWindowlessControl::DisplayModeChanged"]
old-location: dshow\ivmrwindowlesscontrol_displaymodechanged.htm
tech.root: dshow
ms.assetid: 83fbca03-0e8c-4386-96ff-f572f0b13312
ms.date: 12/05/2018
ms.keywords: DisplayModeChanged, DisplayModeChanged method [DirectShow], DisplayModeChanged method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],DisplayModeChanged method, IVMRWindowlessControl.DisplayModeChanged, IVMRWindowlessControl::DisplayModeChanged, IVMRWindowlessControlDisplayModeChanged, dshow.ivmrwindowlesscontrol_displaymodechanged, strmif/IVMRWindowlessControl::DisplayModeChanged
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
 - IVMRWindowlessControl::DisplayModeChanged
 - strmif/IVMRWindowlessControl::DisplayModeChanged
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
 - IVMRWindowlessControl.DisplayModeChanged
---

# IVMRWindowlessControl::DisplayModeChanged


## -description

The <code>DisplayModeChanged</code> method informs the VMR that a WM_DISPLAYCHANGE message has been received by the application.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>

## -remarks

An application must call this method whenever it receives a WM_DISPLAYCHANGE window message, but only if the VMR is currently in windowless mode.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>

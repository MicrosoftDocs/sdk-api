---
UID: NF:wmcodecdsp.IWMResizerProps.SetInterlaceMode
title: IWMResizerProps::SetInterlaceMode (wmcodecdsp.h)
description: The SetInterlaceMode method specifies whether the input video stream is interlaced.
helpviewer_keywords: ["IWMResizerProps interface [Media Foundation]","SetInterlaceMode method","IWMResizerProps.SetInterlaceMode","IWMResizerProps::SetInterlaceMode","SetInterlaceMode","SetInterlaceMode method [Media Foundation]","SetInterlaceMode method [Media Foundation]","IWMResizerProps interface","codecapi.iwmresizerpropssetinterlacemode","mf.iwmresizerpropssetinterlacemode","wmcodecdsp/IWMResizerProps::SetInterlaceMode"]
old-location: mf\iwmresizerpropssetinterlacemode.htm
tech.root: mf
ms.assetid: a5ce36aa-d46c-4c17-bc8d-4840ea496980
ms.date: 12/05/2018
ms.keywords: IWMResizerProps interface [Media Foundation],SetInterlaceMode method, IWMResizerProps.SetInterlaceMode, IWMResizerProps::SetInterlaceMode, SetInterlaceMode, SetInterlaceMode method [Media Foundation], SetInterlaceMode method [Media Foundation],IWMResizerProps interface, codecapi.iwmresizerpropssetinterlacemode, mf.iwmresizerpropssetinterlacemode, wmcodecdsp/IWMResizerProps::SetInterlaceMode
req.header: wmcodecdsp.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMResizerProps::SetInterlaceMode
 - wmcodecdsp/IWMResizerProps::SetInterlaceMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMResizerProps.SetInterlaceMode
---

# IWMResizerProps::SetInterlaceMode


## -description

The <b>SetInterlaceMode</b> method specifies whether the input video stream is interlaced.

## -parameters

### -param lmode [in]

Boolean value. If <b>TRUE</b>, the video is interlaced. If <b>FALSE</b>, the video is progressive.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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

This method is equivalent to setting the <a href="/windows/desktop/medfound/mfpkey-resize-interlace">MFPKEY_RESIZE_INTERLACE</a> property.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops">IWMResizerProps Interface</a>
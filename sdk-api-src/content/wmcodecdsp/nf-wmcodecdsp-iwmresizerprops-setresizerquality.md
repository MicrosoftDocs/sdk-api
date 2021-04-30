---
UID: NF:wmcodecdsp.IWMResizerProps.SetResizerQuality
title: IWMResizerProps::SetResizerQuality (wmcodecdsp.h)
description: Specifies whether to use an algorithm that produces higher-quality video, or a faster algorithm.
helpviewer_keywords: ["IWMResizerProps interface [Media Foundation]","SetResizerQuality method","IWMResizerProps.SetResizerQuality","IWMResizerProps::SetResizerQuality","SetResizerQuality","SetResizerQuality method [Media Foundation]","SetResizerQuality method [Media Foundation]","IWMResizerProps interface","codecapi.iwmresizerpropssetresizerquality","mf.iwmresizerpropssetresizerquality","wmcodecdsp/IWMResizerProps::SetResizerQuality"]
old-location: mf\iwmresizerpropssetresizerquality.htm
tech.root: mf
ms.assetid: 64a85094-4247-41d8-9bb6-bdaedba62c19
ms.date: 12/05/2018
ms.keywords: IWMResizerProps interface [Media Foundation],SetResizerQuality method, IWMResizerProps.SetResizerQuality, IWMResizerProps::SetResizerQuality, SetResizerQuality, SetResizerQuality method [Media Foundation], SetResizerQuality method [Media Foundation],IWMResizerProps interface, codecapi.iwmresizerpropssetresizerquality, mf.iwmresizerpropssetresizerquality, wmcodecdsp/IWMResizerProps::SetResizerQuality
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
 - IWMResizerProps::SetResizerQuality
 - wmcodecdsp/IWMResizerProps::SetResizerQuality
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
 - IWMResizerProps.SetResizerQuality
---

# IWMResizerProps::SetResizerQuality


## -description

Specifies whether to use an algorithm that produces higher-quality video, or a faster algorithm.

## -parameters

### -param lquality [in]

Boolean value. If <b>TRUE</b>, the video resizer uses an algorithm that produces higher-quality video. If <b>FALSE</b>, the video resizer uses a faster algorithm.

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

This method is equivalent to setting the <a href="/windows/desktop/medfound/mfpkey-resize-quality">MFPKEY_RESIZE_QUALITY</a> property.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops">IWMResizerProps Interface</a>
---
UID: NF:wmcodecdsp.IWMResizerProps.SetInterlaceMode
title: IWMResizerProps::SetInterlaceMode (wmcodecdsp.h)
author: windows-sdk-content
description: The SetInterlaceMode method specifies whether the input video stream is interlaced.
old-location: mf\iwmresizerpropssetinterlacemode.htm
tech.root: medfound
ms.assetid: a5ce36aa-d46c-4c17-bc8d-4840ea496980
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMResizerProps interface [Media Foundation],SetInterlaceMode method, IWMResizerProps.SetInterlaceMode, IWMResizerProps::SetInterlaceMode, SetInterlaceMode, SetInterlaceMode method [Media Foundation], SetInterlaceMode method [Media Foundation],IWMResizerProps interface, codecapi.iwmresizerpropssetinterlacemode, mf.iwmresizerpropssetinterlacemode, wmcodecdsp/IWMResizerProps::SetInterlaceMode
ms.topic: method
f1_keywords: 
 - "wmcodecdsp/IWMResizerProps.SetInterlaceMode"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMResizerProps.SetInterlaceMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



This method is equivalent to setting the <a href="https://docs.microsoft.com/windows/desktop/medfound/mfpkey-resize-interlace">MFPKEY_RESIZE_INTERLACE</a> property. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops">IWMResizerProps Interface</a>
 

 


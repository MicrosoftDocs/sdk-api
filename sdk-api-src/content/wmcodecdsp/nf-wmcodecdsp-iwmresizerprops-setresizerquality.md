---
UID: NF:wmcodecdsp.IWMResizerProps.SetResizerQuality
title: IWMResizerProps::SetResizerQuality
author: windows-sdk-content
description: Specifies whether to use an algorithm that produces higher-quality video, or a faster algorithm.
old-location: mf\iwmresizerpropssetresizerquality.htm
old-project: medfound
ms.assetid: 64a85094-4247-41d8-9bb6-bdaedba62c19
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IWMResizerProps interface [Media Foundation],SetResizerQuality method, IWMResizerProps.SetResizerQuality, IWMResizerProps::SetResizerQuality, SetResizerQuality, SetResizerQuality method [Media Foundation], SetResizerQuality method [Media Foundation],IWMResizerProps interface, codecapi.iwmresizerpropssetresizerquality, mf.iwmresizerpropssetresizerquality, wmcodecdsp/IWMResizerProps::SetResizerQuality
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MFVideoDSPMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMResizerProps.SetResizerQuality
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



This method is equivalent to setting the <a href="https://msdn.microsoft.com/a6760e7e-7c99-4412-bde5-05958fad89a1">MFPKEY_RESIZE_QUALITY</a> property. 




## -see-also




<a href="https://msdn.microsoft.com/12c26507-c729-4143-a0bd-e043d42744f6">IWMResizerProps Interface</a>
 

 


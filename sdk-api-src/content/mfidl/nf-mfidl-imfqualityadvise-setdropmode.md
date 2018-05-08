---
UID: NF:mfidl.IMFQualityAdvise.SetDropMode
title: IMFQualityAdvise::SetDropMode
author: windows-driver-content
description: Sets the drop mode. In drop mode, a component drops samples, more or less aggressively depending on the level of the drop mode.
old-location: mf\imfqualityadvise_setdropmode.htm
old-project: medfound
ms.assetid: 190de66a-6c47-49d5-a8f6-c2fb57a7aee2
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 190de66a-6c47-49d5-a8f6-c2fb57a7aee2, IMFQualityAdvise interface [Media Foundation],SetDropMode method, IMFQualityAdvise.SetDropMode, IMFQualityAdvise::SetDropMode, SetDropMode, SetDropMode method [Media Foundation], SetDropMode method [Media Foundation],IMFQualityAdvise interface, mf.imfqualityadvise_setdropmode, mfidl/IMFQualityAdvise::SetDropMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFQualityAdvise.SetDropMode
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFQualityAdvise::SetDropMode


## -description



Sets the drop mode. In drop mode, a component drops samples, more or less aggressively depending on the level of the drop mode.




## -parameters




### -param eDropMode [in]

Requested drop mode, specified as a member of the <a href="https://msdn.microsoft.com/e40751d2-9abf-4fe6-8829-9b1fbf4531e8">MF_QUALITY_DROP_MODE</a> enumeration.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_MORE_DROP_MODES</b></dt>
</dl>
</td>
<td width="60%">
The component does not support the specified mode or any higher modes.

</td>
</tr>
</table>
 




## -remarks



If this method is called on a media source, the media source might switch between thinned and non-thinned output. If that occurs, the affected streams will send an <a href="https://msdn.microsoft.com/7de8cb64-122a-475f-990c-c19590a9d9d8">MEStreamThinMode</a> event to indicate the transition. The operation is asynchronous; after <b>SetDropMode</b> returns, you might receive samples that were queued before the transition. The MEStreamThinMode event marks the exact point in the stream where the transition occurs.




## -see-also




<a href="https://msdn.microsoft.com/20681ce7-e07e-4e34-9238-ec23cc6bfc84">IMFQualityAdvise</a>
 

 


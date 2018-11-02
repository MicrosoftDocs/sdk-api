---
UID: NF:mfidl.IMFQualityAdvise.GetQualityLevel
title: IMFQualityAdvise::GetQualityLevel
author: windows-sdk-content
description: Retrieves the current quality level.
old-location: mf\imfqualityadvise_getqualitylevel.htm
tech.root: medfound
ms.assetid: 9a2b501e-543d-4ba0-86a1-a55e7d136685
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 9a2b501e-543d-4ba0-86a1-a55e7d136685, GetQualityLevel, GetQualityLevel method [Media Foundation], GetQualityLevel method [Media Foundation],IMFQualityAdvise interface, IMFQualityAdvise interface [Media Foundation],GetQualityLevel method, IMFQualityAdvise.GetQualityLevel, IMFQualityAdvise::GetQualityLevel, mf.imfqualityadvise_getqualitylevel, mfidl/IMFQualityAdvise::GetQualityLevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFQualityAdvise.GetQualityLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFQualityAdvise::GetQualityLevel


## -description



Retrieves the current quality level.




## -parameters




### -param peQualityLevel [out]

Receives the quality level, specified as a member of the <a href="https://msdn.microsoft.com/6fe5abbb-c079-4d74-9c75-6fb502054546">MF_QUALITY_LEVEL</a> enumeration.


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
 




## -see-also




<a href="https://msdn.microsoft.com/20681ce7-e07e-4e34-9238-ec23cc6bfc84">IMFQualityAdvise</a>
 

 


---
UID: NF:mfidl.IMFQualityAdvise.SetQualityLevel
title: IMFQualityAdvise::SetQualityLevel
author: windows-sdk-content
description: Sets the quality level. The quality level determines how the component consumes or produces samples.
old-location: mf\imfqualityadvise_setqualitylevel.htm
tech.root: medfound
ms.assetid: f788fd7d-65fc-4917-8d5d-cfaf35a013e7
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFQualityAdvise interface [Media Foundation],SetQualityLevel method, IMFQualityAdvise.SetQualityLevel, IMFQualityAdvise::SetQualityLevel, SetQualityLevel, SetQualityLevel method [Media Foundation], SetQualityLevel method [Media Foundation],IMFQualityAdvise interface, f788fd7d-65fc-4917-8d5d-cfaf35a013e7, mf.imfqualityadvise_setqualitylevel, mfidl/IMFQualityAdvise::SetQualityLevel
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
 - IMFQualityAdvise.SetQualityLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFQualityAdvise::SetQualityLevel


## -description



Sets the quality level. The quality level determines how the component consumes or produces samples.




## -parameters




### -param eQualityLevel [in]

Requested quality level, specified as a member of the <a href="https://msdn.microsoft.com/6fe5abbb-c079-4d74-9c75-6fb502054546">MF_QUALITY_LEVEL</a> enumeration.


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
<dt><b>MF_E_NO_MORE_QUALITY_LEVELS</b></dt>
</dl>
</td>
<td width="60%">
The component does not support the specified quality level or any levels below it.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/20681ce7-e07e-4e34-9238-ec23cc6bfc84">IMFQualityAdvise</a>
 

 


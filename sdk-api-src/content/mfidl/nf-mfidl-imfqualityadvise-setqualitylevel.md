---
UID: NF:mfidl.IMFQualityAdvise.SetQualityLevel
title: IMFQualityAdvise::SetQualityLevel (mfidl.h)
description: Sets the quality level. The quality level determines how the component consumes or produces samples.
helpviewer_keywords: ["IMFQualityAdvise interface [Media Foundation]","SetQualityLevel method","IMFQualityAdvise.SetQualityLevel","IMFQualityAdvise::SetQualityLevel","SetQualityLevel","SetQualityLevel method [Media Foundation]","SetQualityLevel method [Media Foundation]","IMFQualityAdvise interface","f788fd7d-65fc-4917-8d5d-cfaf35a013e7","mf.imfqualityadvise_setqualitylevel","mfidl/IMFQualityAdvise::SetQualityLevel"]
old-location: mf\imfqualityadvise_setqualitylevel.htm
tech.root: mf
ms.assetid: f788fd7d-65fc-4917-8d5d-cfaf35a013e7
ms.date: 12/05/2018
ms.keywords: IMFQualityAdvise interface [Media Foundation],SetQualityLevel method, IMFQualityAdvise.SetQualityLevel, IMFQualityAdvise::SetQualityLevel, SetQualityLevel, SetQualityLevel method [Media Foundation], SetQualityLevel method [Media Foundation],IMFQualityAdvise interface, f788fd7d-65fc-4917-8d5d-cfaf35a013e7, mf.imfqualityadvise_setqualitylevel, mfidl/IMFQualityAdvise::SetQualityLevel
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFQualityAdvise::SetQualityLevel
 - mfidl/IMFQualityAdvise::SetQualityLevel
dev_langs:
 - c++
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
---

# IMFQualityAdvise::SetQualityLevel


## -description

Sets the quality level. The quality level determines how the component consumes or produces samples.

## -parameters

### -param eQualityLevel [in]

Requested quality level, specified as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_quality_level">MF_QUALITY_LEVEL</a> enumeration.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>
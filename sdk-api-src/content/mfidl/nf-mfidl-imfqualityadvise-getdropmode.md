---
UID: NF:mfidl.IMFQualityAdvise.GetDropMode
title: IMFQualityAdvise::GetDropMode (mfidl.h)
description: Retrieves the current drop mode.
helpviewer_keywords: ["GetDropMode","GetDropMode method [Media Foundation]","GetDropMode method [Media Foundation]","IMFQualityAdvise interface","IMFQualityAdvise interface [Media Foundation]","GetDropMode method","IMFQualityAdvise.GetDropMode","IMFQualityAdvise::GetDropMode","bb700a3e-837f-4e88-a9b7-294c41143402","mf.imfqualityadvise_getdropmode","mfidl/IMFQualityAdvise::GetDropMode"]
old-location: mf\imfqualityadvise_getdropmode.htm
tech.root: mf
ms.assetid: bb700a3e-837f-4e88-a9b7-294c41143402
ms.date: 12/05/2018
ms.keywords: GetDropMode, GetDropMode method [Media Foundation], GetDropMode method [Media Foundation],IMFQualityAdvise interface, IMFQualityAdvise interface [Media Foundation],GetDropMode method, IMFQualityAdvise.GetDropMode, IMFQualityAdvise::GetDropMode, bb700a3e-837f-4e88-a9b7-294c41143402, mf.imfqualityadvise_getdropmode, mfidl/IMFQualityAdvise::GetDropMode
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
 - IMFQualityAdvise::GetDropMode
 - mfidl/IMFQualityAdvise::GetDropMode
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
 - IMFQualityAdvise.GetDropMode
---

# IMFQualityAdvise::GetDropMode


## -description

Retrieves the current drop mode.

## -parameters

### -param peDropMode [out]

Receives the drop mode, specified as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_quality_drop_mode">MF_QUALITY_DROP_MODE</a> enumeration.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>
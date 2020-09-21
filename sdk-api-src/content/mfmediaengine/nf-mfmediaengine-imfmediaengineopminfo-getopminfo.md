---
UID: NF:mfmediaengine.IMFMediaEngineOPMInfo.GetOPMInfo
title: IMFMediaEngineOPMInfo::GetOPMInfo (mfmediaengine.h)
description: Gets status information about the Output Protection Manager (OPM).
helpviewer_keywords: ["GetOPMInfo","GetOPMInfo method [Media Foundation]","GetOPMInfo method [Media Foundation]","IMFMediaEngineOPMInfo interface","IMFMediaEngineOPMInfo interface [Media Foundation]","GetOPMInfo method","IMFMediaEngineOPMInfo.GetOPMInfo","IMFMediaEngineOPMInfo::GetOPMInfo","mf.imfmediaengineopminfo_getopminfo","mfmediaengine/IMFMediaEngineOPMInfo::GetOPMInfo"]
old-location: mf\imfmediaengineopminfo_getopminfo.htm
tech.root: mf
ms.assetid: 5e4a6e8f-5042-4de1-8cea-64b8e6cc928a
ms.date: 12/05/2018
ms.keywords: GetOPMInfo, GetOPMInfo method [Media Foundation], GetOPMInfo method [Media Foundation],IMFMediaEngineOPMInfo interface, IMFMediaEngineOPMInfo interface [Media Foundation],GetOPMInfo method, IMFMediaEngineOPMInfo.GetOPMInfo, IMFMediaEngineOPMInfo::GetOPMInfo, mf.imfmediaengineopminfo_getopminfo, mfmediaengine/IMFMediaEngineOPMInfo::GetOPMInfo
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFMediaEngineOPMInfo::GetOPMInfo
 - mfmediaengine/IMFMediaEngineOPMInfo::GetOPMInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineOPMInfo.GetOPMInfo
---

# IMFMediaEngineOPMInfo::GetOPMInfo


## -description

Gets status information about the   <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>  (OPM).

## -parameters

### -param pStatus [out]

        A pointer to a <a href="/windows/desktop/medfound/mf-media-engine-opm-status">MF_MEDIA_ENGINE_OPM_STATUS</a> enum type that indicates the OPM status.

### -param pConstricted [out]

A pointer to a <b>BOOL</b> type that indicates the constriction status.

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
The method succeeded

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
If any of the parameters are <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineopminfo">IMFMediaEngineOPMInfo</a>
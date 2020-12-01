---
UID: NF:wmcontainer.IMFASFStreamConfig.SetStreamNumber
title: IMFASFStreamConfig::SetStreamNumber (wmcontainer.h)
description: Assigns a stream number to the stream.
helpviewer_keywords: ["5b22d857-fced-4094-a0ad-891f3ccf8b18","IMFASFStreamConfig interface [Media Foundation]","SetStreamNumber method","IMFASFStreamConfig.SetStreamNumber","IMFASFStreamConfig::SetStreamNumber","SetStreamNumber","SetStreamNumber method [Media Foundation]","SetStreamNumber method [Media Foundation]","IMFASFStreamConfig interface","mf.imfasfstreamconfig_setstreamnumber","wmcontainer/IMFASFStreamConfig::SetStreamNumber"]
old-location: mf\imfasfstreamconfig_setstreamnumber.htm
tech.root: mf
ms.assetid: 5b22d857-fced-4094-a0ad-891f3ccf8b18
ms.date: 12/05/2018
ms.keywords: 5b22d857-fced-4094-a0ad-891f3ccf8b18, IMFASFStreamConfig interface [Media Foundation],SetStreamNumber method, IMFASFStreamConfig.SetStreamNumber, IMFASFStreamConfig::SetStreamNumber, SetStreamNumber, SetStreamNumber method [Media Foundation], SetStreamNumber method [Media Foundation],IMFASFStreamConfig interface, mf.imfasfstreamconfig_setstreamnumber, wmcontainer/IMFASFStreamConfig::SetStreamNumber
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFASFStreamConfig::SetStreamNumber
 - wmcontainer/IMFASFStreamConfig::SetStreamNumber
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
 - IMFASFStreamConfig.SetStreamNumber
---

# IMFASFStreamConfig::SetStreamNumber


## -description

Assigns a stream number to the stream.

## -parameters

### -param wStreamNum [in]

The number to assign to the stream.

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

Stream numbers start from 1 and do not need to be sequential.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a>
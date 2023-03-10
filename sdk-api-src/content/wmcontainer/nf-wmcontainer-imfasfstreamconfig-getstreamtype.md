---
UID: NF:wmcontainer.IMFASFStreamConfig.GetStreamType
title: IMFASFStreamConfig::GetStreamType (wmcontainer.h)
description: Gets the major media type of the stream.
helpviewer_keywords: ["5f085107-f205-47ab-acb5-d45a881ce76c","GetStreamType","GetStreamType method [Media Foundation]","GetStreamType method [Media Foundation]","IMFASFStreamConfig interface","IMFASFStreamConfig interface [Media Foundation]","GetStreamType method","IMFASFStreamConfig.GetStreamType","IMFASFStreamConfig::GetStreamType","mf.imfasfstreamconfig_getstreamtype","wmcontainer/IMFASFStreamConfig::GetStreamType"]
old-location: mf\imfasfstreamconfig_getstreamtype.htm
tech.root: mf
ms.assetid: 5f085107-f205-47ab-acb5-d45a881ce76c
ms.date: 12/05/2018
ms.keywords: 5f085107-f205-47ab-acb5-d45a881ce76c, GetStreamType, GetStreamType method [Media Foundation], GetStreamType method [Media Foundation],IMFASFStreamConfig interface, IMFASFStreamConfig interface [Media Foundation],GetStreamType method, IMFASFStreamConfig.GetStreamType, IMFASFStreamConfig::GetStreamType, mf.imfasfstreamconfig_getstreamtype, wmcontainer/IMFASFStreamConfig::GetStreamType
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
 - IMFASFStreamConfig::GetStreamType
 - wmcontainer/IMFASFStreamConfig::GetStreamType
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
 - IMFASFStreamConfig.GetStreamType
---

# IMFASFStreamConfig::GetStreamType


## -description

Gets the major media type of the stream.

## -parameters

### -param pguidStreamType [out]

Receives the major media type for the stream. For a list of possible values, see <a href="/windows/desktop/medfound/media-type-guids">Major Media Types</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>
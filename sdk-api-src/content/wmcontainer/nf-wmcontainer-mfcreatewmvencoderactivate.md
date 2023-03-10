---
UID: NF:wmcontainer.MFCreateWMVEncoderActivate
title: MFCreateWMVEncoderActivate function (wmcontainer.h)
description: Creates an activation object that can be used to create a Windows Media Video (WMV) encoder.
helpviewer_keywords: ["MFCreateWMVEncoderActivate","MFCreateWMVEncoderActivate function [Media Foundation]","f818dba1-e28f-4fd4-813d-33f638d979d7","mf.mfcreatewmvencoderactivate","wmcontainer/MFCreateWMVEncoderActivate"]
old-location: mf\mfcreatewmvencoderactivate.htm
tech.root: mf
ms.assetid: f818dba1-e28f-4fd4-813d-33f638d979d7
ms.date: 12/05/2018
ms.keywords: MFCreateWMVEncoderActivate, MFCreateWMVEncoderActivate function [Media Foundation], f818dba1-e28f-4fd4-813d-33f638d979d7, mf.mfcreatewmvencoderactivate, wmcontainer/MFCreateWMVEncoderActivate
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateWMVEncoderActivate
 - wmcontainer/MFCreateWMVEncoderActivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateWMVEncoderActivate
---

# MFCreateWMVEncoderActivate function


## -description

Creates an activation object that can be used to create a Windows Media Video (WMV) encoder.

## -parameters

### -param pMediaType

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. This parameter specifies the encoded output format.

### -param pEncodingConfigurationProperties

A pointer to the <b>IPropertyStore</b> interface of a property store that contains encoding parameters. Encoding parameters for the WMV encoder are defined in the header file wmcodecdsp.h. If you have an ASF ContentInfo object that contains an ASF profile object with all the streams for the output file, you can get the property store by calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore">IMFASFContentInfo::GetEncodingConfigurationPropertyStore</a>.

### -param ppActivate

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface. Use this interface to create the encoder. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
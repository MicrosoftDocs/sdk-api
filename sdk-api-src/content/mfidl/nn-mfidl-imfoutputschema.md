---
UID: NN:mfidl.IMFOutputSchema
title: IMFOutputSchema (mfidl.h)
description: Encapsulates information about an output protection system and its corresponding configuration data.
helpviewer_keywords: ["IMFOutputSchema","IMFOutputSchema interface [Media Foundation]","IMFOutputSchema interface [Media Foundation]","described","d0786628-dde9-43a9-8e81-0b0c396ad426","mf.imfoutputschema","mfidl/IMFOutputSchema"]
old-location: mf\imfoutputschema.htm
tech.root: mf
ms.assetid: d0786628-dde9-43a9-8e81-0b0c396ad426
ms.date: 12/05/2018
ms.keywords: IMFOutputSchema, IMFOutputSchema interface [Media Foundation], IMFOutputSchema interface [Media Foundation],described, d0786628-dde9-43a9-8e81-0b0c396ad426, mf.imfoutputschema, mfidl/IMFOutputSchema
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
 - IMFOutputSchema
 - mfidl/IMFOutputSchema
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
 - IMFOutputSchema
---

# IMFOutputSchema interface


## -description

Encapsulates information about an output protection system and its corresponding configuration data.

## -inheritance

The <b>IMFOutputSchema</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFOutputSchema</b> also has these types of members:

## -remarks

If the configuration information for the output protection system does not require more than a <b>DWORD</b> of space, the configuration information is retrieved in the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata">GetConfigurationData</a> method. If more than a <b>DWORD</b> of configuration information is needed, it is stored using the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

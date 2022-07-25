---
UID: NN:imapi2.IWriteSpeedDescriptor
title: IWriteSpeedDescriptor (imapi2.h)
description: Use this interface retrieve detailed write configurations supported by the disc recorder and current media, for example, the media type, write speed, rotational-speed control type.
helpviewer_keywords: ["IWriteSpeedDescriptor","IWriteSpeedDescriptor interface [IMAPI]","IWriteSpeedDescriptor interface [IMAPI]","described","imapi.iwritespeeddescriptor","imapi2/IWriteSpeedDescriptor"]
old-location: imapi\iwritespeeddescriptor.htm
tech.root: imapi
ms.assetid: 9efaa744-ae0c-4101-8d78-091cba990533
ms.date: 12/05/2018
ms.keywords: IWriteSpeedDescriptor, IWriteSpeedDescriptor interface [IMAPI], IWriteSpeedDescriptor interface [IMAPI],described, imapi.iwritespeeddescriptor, imapi2/IWriteSpeedDescriptor
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IWriteSpeedDescriptor
 - imapi2/IWriteSpeedDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IWriteSpeedDescriptor
---

# IWriteSpeedDescriptor interface


## -description

Use this interface retrieve detailed write configurations supported by the disc recorder and current media, for example, the media type, write speed, rotational-speed control type.

To get this interface, call one of the following methods:<ul>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_supportedwritespeeddescriptors">IDiscFormat2Data::get_SupportedWriteSpeedDescriptors</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_supportedwritespeeddescriptors">IDiscFormat2RawCD::get_SupportedWriteSpeedDescriptors</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_supportedwritespeeddescriptors">IDiscFormat2TrackAtOnce::get_SupportedWriteSpeedDescriptors</a>
</li>
</ul>

## -inheritance

The <b>IWriteSpeedDescriptor</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWriteSpeedDescriptor</b> also has these types of members:

## -remarks

This is a <b>MsftWriteSpeedDescriptor</b> object in script.

## -see-also

<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_supportedwritespeeddescriptors">IDiscFormat2Data::get_SupportedWriteSpeedDescriptors</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_supportedwritespeeddescriptors">IDiscFormat2RawCD::get_SupportedWriteSpeedDescriptors</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_supportedwritespeeddescriptors">IDiscFormat2TrackAtOnce::get_SupportedWriteSpeedDescriptors</a>

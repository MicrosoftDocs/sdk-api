---
UID: NN:wmcontainer.IMFASFProfile
title: IMFASFProfile (wmcontainer.h)
description: Manages an Advanced Systems Format (ASF) profile.
helpviewer_keywords: ["IMFASFProfile","IMFASFProfile interface [Media Foundation]","IMFASFProfile interface [Media Foundation]","described","fe441c61-1be7-4fda-a2a3-bd79ecf4e54c","mf.imfasfprofile","wmcontainer/IMFASFProfile"]
old-location: mf\imfasfprofile.htm
tech.root: mf
ms.assetid: fe441c61-1be7-4fda-a2a3-bd79ecf4e54c
ms.date: 12/05/2018
ms.keywords: IMFASFProfile, IMFASFProfile interface [Media Foundation], IMFASFProfile interface [Media Foundation],described, fe441c61-1be7-4fda-a2a3-bd79ecf4e54c, mf.imfasfprofile, wmcontainer/IMFASFProfile
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
 - IMFASFProfile
 - wmcontainer/IMFASFProfile
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
 - IMFASFProfile
---

# IMFASFProfile interface


## -description

Manages an Advanced Systems Format (ASF) profile. A profile is a collection of information that describes the configuration of streams that will be included in an ASF file. Information about the relationships between streams is also included in the profile.

An <b>IMFASFProfile</b> interface exists for every ASF profile object. To create an ASF profile object, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile">MFCreateASFProfile</a> or <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor">MFCreateASFProfileFromPresentationDescriptor</a>.

## -inheritance

The <b>IMFASFProfile</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFASFProfile</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

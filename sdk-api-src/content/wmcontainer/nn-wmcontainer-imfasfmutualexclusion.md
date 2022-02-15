---
UID: NN:wmcontainer.IMFASFMutualExclusion
title: IMFASFMutualExclusion (wmcontainer.h)
description: Configures an Advanced Systems Format (ASF) mutual exclusion object, which manages information about a group of streams in an ASF profile that are mutually exclusive.
helpviewer_keywords: ["9c2278ec-77d1-445e-94bc-44e5d48f14ae","IMFASFMutualExclusion","IMFASFMutualExclusion interface [Media Foundation]","IMFASFMutualExclusion interface [Media Foundation]","described","mf.imfasfmutualexclusion","wmcontainer/IMFASFMutualExclusion"]
old-location: mf\imfasfmutualexclusion.htm
tech.root: mf
ms.assetid: 9c2278ec-77d1-445e-94bc-44e5d48f14ae
ms.date: 12/05/2018
ms.keywords: 9c2278ec-77d1-445e-94bc-44e5d48f14ae, IMFASFMutualExclusion, IMFASFMutualExclusion interface [Media Foundation], IMFASFMutualExclusion interface [Media Foundation],described, mf.imfasfmutualexclusion, wmcontainer/IMFASFMutualExclusion
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
 - IMFASFMutualExclusion
 - wmcontainer/IMFASFMutualExclusion
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
 - IMFASFMutualExclusion
---

# IMFASFMutualExclusion interface


## -description

Configures an Advanced Systems Format (ASF) mutual exclusion object, which manages information about a group of streams in an ASF profile that are mutually exclusive. When streams or groups of streams are mutually exclusive, only one of them is read at a time, they are not read concurrently.

A common example of mutual exclusion is a set of streams that each include the same content encoded at a different bit rate. The stream that is used is determined by the available bandwidth to the reader.

An <b>IMFASFMutualExclusion</b> interface exists for every ASF mutual exclusion object. A pointer to this interface is obtained when you create the object using the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion">IMFASFProfile::CreateMutualExclusion</a> method.

## -inheritance

The <b>IMFASFMutualExclusion</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFMutualExclusion</b> also has these types of members:

## -remarks

An ASF profile object can support multiple mutual exclusions. Each must be configured using a separate ASF mutual exclusion object.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/using-mutual-exclusion-for-asf-streams">Using Mutual Exclusion for ASF Streams</a>

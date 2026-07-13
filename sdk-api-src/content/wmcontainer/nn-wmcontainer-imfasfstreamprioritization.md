---
UID: NN:wmcontainer.IMFASFStreamPrioritization
title: IMFASFStreamPrioritization (wmcontainer.h)
description: Not implemented. (IMFASFStreamPrioritization)
helpviewer_keywords: ["6eb79c52-dc81-406c-9000-d25ad380e6b2","IMFASFStreamPrioritization","IMFASFStreamPrioritization interface [Media Foundation]","IMFASFStreamPrioritization interface [Media Foundation]","described","mf.imfasfstreamprioritization","wmcontainer/IMFASFStreamPrioritization"]
old-location: mf\imfasfstreamprioritization.htm
tech.root: mf
ms.assetid: 6eb79c52-dc81-406c-9000-d25ad380e6b2
ms.date: 12/05/2018
ms.keywords: 6eb79c52-dc81-406c-9000-d25ad380e6b2, IMFASFStreamPrioritization, IMFASFStreamPrioritization interface [Media Foundation], IMFASFStreamPrioritization interface [Media Foundation],described, mf.imfasfstreamprioritization, wmcontainer/IMFASFStreamPrioritization
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
 - IMFASFStreamPrioritization
 - wmcontainer/IMFASFStreamPrioritization
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
 - IMFASFStreamPrioritization
---

# IMFASFStreamPrioritization interface


## -description

<div class="alert"><b>Note</b>  This interface is not implemented.</div><div> </div>Manages information about the relative priorities of a group of streams in an Advanced Systems Format (ASF) profile. This interface manages information about the relative priorities of a group of streams in an ASF profile. Priority is used in streaming to determine which streams should be dropped first when available bandwidth decreases.

The ASF stream prioritization object exposes this interface. The stream prioritization object maintains a list of stream numbers in priority order. The methods of this interface manipulate and interrogate that list. To obtain a pointer to this interface, call the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstreamprioritization">IMFASFProfile::CreateStreamPrioritization</a> method.

## -inheritance

The <b>IMFASFStreamPrioritization</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFStreamPrioritization</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

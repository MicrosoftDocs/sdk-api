---
UID: NN:wmcontainer.IMFASFStreamSelector
title: IMFASFStreamSelector (wmcontainer.h)
description: Selects streams in an Advanced Systems Format (ASF) file, based on the mutual exclusion information in the ASF header.
helpviewer_keywords: ["IMFASFStreamSelector","IMFASFStreamSelector interface [Media Foundation]","IMFASFStreamSelector interface [Media Foundation]","described","d2e1fc15-2e12-4698-a4b1-ca8046d228de","mf.imfasfstreamselector","wmcontainer/IMFASFStreamSelector"]
old-location: mf\imfasfstreamselector.htm
tech.root: mf
ms.assetid: d2e1fc15-2e12-4698-a4b1-ca8046d228de
ms.date: 12/05/2018
ms.keywords: IMFASFStreamSelector, IMFASFStreamSelector interface [Media Foundation], IMFASFStreamSelector interface [Media Foundation],described, d2e1fc15-2e12-4698-a4b1-ca8046d228de, mf.imfasfstreamselector, wmcontainer/IMFASFStreamSelector
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
 - IMFASFStreamSelector
 - wmcontainer/IMFASFStreamSelector
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
 - IMFASFStreamSelector
---

# IMFASFStreamSelector interface


## -description

Selects streams in an Advanced Systems Format (ASF) file, based on the mutual exclusion information in the ASF header. The ASF stream selector object exposes this interface. To create the ASF stream selector, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfstreamselector">MFCreateASFStreamSelector</a>.

## -inheritance

The <b>IMFASFStreamSelector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFStreamSelector</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

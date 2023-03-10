---
UID: NN:mfidl.IMFSAMIStyle
title: IMFSAMIStyle (mfidl.h)
description: Sets and retrieves Synchronized Accessible Media Interchange (SAMI) styles on the SAMI Media Source.
helpviewer_keywords: ["IMFSAMIStyle","IMFSAMIStyle interface [Media Foundation]","IMFSAMIStyle interface [Media Foundation]","described","c4887c52-57af-4783-b853-11fe6ad3510e","mf.imfsamistyle","mfidl/IMFSAMIStyle"]
old-location: mf\imfsamistyle.htm
tech.root: mf
ms.assetid: c4887c52-57af-4783-b853-11fe6ad3510e
ms.date: 12/05/2018
ms.keywords: IMFSAMIStyle, IMFSAMIStyle interface [Media Foundation], IMFSAMIStyle interface [Media Foundation],described, c4887c52-57af-4783-b853-11fe6ad3510e, mf.imfsamistyle, mfidl/IMFSAMIStyle
req.header: mfidl.h
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
 - IMFSAMIStyle
 - mfidl/IMFSAMIStyle
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
 - IMFSAMIStyle
---

# IMFSAMIStyle interface


## -description

Sets and retrieves Synchronized Accessible Media Interchange (SAMI) styles on the <a href="/windows/desktop/medfound/sami-media-source">SAMI Media Source</a>.

## -inheritance

The <b>IMFSAMIStyle</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSAMIStyle</b> also has these types of members:

## -remarks

To get a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier is <b>MF_SAMI_SERVICE</b>. Call <b>GetService</b> either directly on the SAMI media source, or on the Media Session (if you are using the SAMI source with the Media Session).

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/sami-media-source">SAMI Media Source</a>

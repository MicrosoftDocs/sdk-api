---
UID: NN:opmapi.IOPMVideoOutput
title: IOPMVideoOutput (opmapi.h)
description: Represents a video output for an Output Protection Manager (OPM) session.
helpviewer_keywords: ["IOPMVideoOutput","IOPMVideoOutput interface [Media Foundation]","IOPMVideoOutput interface [Media Foundation]","described","mf.iopmvideooutput","opmapi/IOPMVideoOutput"]
old-location: mf\iopmvideooutput.htm
tech.root: mf
ms.assetid: 8bf43577-3535-4f62-ac81-bb7e3c329403
ms.date: 12/05/2018
ms.keywords: IOPMVideoOutput, IOPMVideoOutput interface [Media Foundation], IOPMVideoOutput interface [Media Foundation],described, mf.iopmvideooutput, opmapi/IOPMVideoOutput
req.header: opmapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOPMVideoOutput
 - opmapi/IOPMVideoOutput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - opmapi.h
api_name:
 - IOPMVideoOutput
---

# IOPMVideoOutput interface


## -description

Represents a video output for an <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM) session.

To get a pointer to this interface, call one of the following functions:
<ul>
<li>
<a href="/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object">OPMGetVideoOutputsFromIDirect3DDevice9Object</a>
</li>
<li>
<a href="/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor">OPMGetVideoOutputsFromHMONITOR</a>
</li>
</ul>

## -inheritance

The <b>IOPMVideoOutput</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOPMVideoOutput</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/opm-interfaces">OPM Interfaces</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>

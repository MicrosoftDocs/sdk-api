---
UID: NN:opmapi.IOPMVideoOutput
title: IOPMVideoOutput (opmapi.h)

description: Represents a video output for an Output Protection Manager (OPM) session.
old-location: mf\iopmvideooutput.htm
tech.root: medfound
ms.assetid: 8bf43577-3535-4f62-ac81-bb7e3c329403

ms.date: 12/05/2018
ms.keywords: IOPMVideoOutput, IOPMVideoOutput interface [Media Foundation], IOPMVideoOutput interface [Media Foundation],described, mf.iopmvideooutput, opmapi/IOPMVideoOutput
ms.topic: interface
f1_keywords: 
 - "opmapi/IOPMVideoOutput"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - opmapi.h
api_name:
 - IOPMVideoOutput
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOPMVideoOutput interface


## -description


Represents a video output for an <a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM) session.

To get a pointer to this interface, call one of the following functions:
<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object">OPMGetVideoOutputsFromIDirect3DDevice9Object</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor">OPMGetVideoOutputsFromHMONITOR</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOPMVideoOutput</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOPMVideoOutput</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOPMVideoOutput</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure">Configure</a>
</td>
<td align="left" width="63%">
Configures a video output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation">COPPCompatibleGetInformation</a>
</td>
<td align="left" width="63%">
Sends a status request to the display driver. Use this method when OPM is emulating Certified Output Protection Manager (COPP).



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization">FinishIntialization</a>
</td>
<td align="left" width="63%">
Completes the initialization sequence for an OPM session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation">GetInformation</a>
</td>
<td align="left" width="63%">
Sends a status request to the display driver.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization">StartInitialization</a>
</td>
<td align="left" width="63%">
Begins the initialization sequence for an OPM session.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/opm-interfaces">OPM Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
 

 


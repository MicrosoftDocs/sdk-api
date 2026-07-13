---
UID: NF:mfmp2dlna.IMFDLNASinkInit.Initialize
title: IMFDLNASinkInit::Initialize (mfmp2dlna.h)
description: Initializes the Digital Living Network Alliance (DLNA) media sink. (IMFDLNASinkInit.Initialize)
helpviewer_keywords: ["IMFDLNASinkInit interface [Media Foundation]","Initialize method","IMFDLNASinkInit.Initialize","IMFDLNASinkInit::Initialize","Initialize","Initialize method [Media Foundation]","Initialize method [Media Foundation]","IMFDLNASinkInit interface","mf.imfdlnasinkinit_initialize","mfmp2dlna/IMFDLNASinkInit::Initialize"]
old-location: mf\imfdlnasinkinit_initialize.htm
tech.root: mf
ms.assetid: 48c3842c-7d88-4232-b882-363d9310ffe8
ms.date: 12/05/2018
ms.keywords: IMFDLNASinkInit interface [Media Foundation],Initialize method, IMFDLNASinkInit.Initialize, IMFDLNASinkInit::Initialize, Initialize, Initialize method [Media Foundation], Initialize method [Media Foundation],IMFDLNASinkInit interface, mf.imfdlnasinkinit_initialize, mfmp2dlna/IMFDLNASinkInit::Initialize
req.header: mfmp2dlna.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFDLNASinkInit::Initialize
 - mfmp2dlna/IMFDLNASinkInit::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmp2dlna.h
api_name:
 - IMFDLNASinkInit.Initialize
---

# IMFDLNASinkInit::Initialize


## -description

Initializes the Digital Living Network Alliance (DLNA) media sink.

## -parameters

### -param pByteStream [in]

Pointer to a byte stream. The DLNA media sink writes data to this byte stream. The byte stream must be writable.

### -param fPal [in]

If <b>TRUE</b>, the DLNA media sink accepts PAL video formats. Otherwise, it accepts NTSC video  formats.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The method was already called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">IMFMediaSink::Shutdown</a> method was called.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfmp2dlna/nn-mfmp2dlna-imfdlnasinkinit">IMFDLNASinkInit</a>

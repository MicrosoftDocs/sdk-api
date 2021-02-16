---
UID: NF:wmcontainer.IMFASFMultiplexer.Initialize
title: IMFASFMultiplexer::Initialize (wmcontainer.h)
description: Initializes the multiplexer with the data from an ASF ContentInfo object.
helpviewer_keywords: ["61c37bd5-3f6f-434b-ae5b-c25c5213d49f","IMFASFMultiplexer interface [Media Foundation]","Initialize method","IMFASFMultiplexer.Initialize","IMFASFMultiplexer::Initialize","Initialize","Initialize method [Media Foundation]","Initialize method [Media Foundation]","IMFASFMultiplexer interface","mf.imfasfmultiplexer_initialize","wmcontainer/IMFASFMultiplexer::Initialize"]
old-location: mf\imfasfmultiplexer_initialize.htm
tech.root: mf
ms.assetid: 61c37bd5-3f6f-434b-ae5b-c25c5213d49f
ms.date: 12/05/2018
ms.keywords: 61c37bd5-3f6f-434b-ae5b-c25c5213d49f, IMFASFMultiplexer interface [Media Foundation],Initialize method, IMFASFMultiplexer.Initialize, IMFASFMultiplexer::Initialize, Initialize, Initialize method [Media Foundation], Initialize method [Media Foundation],IMFASFMultiplexer interface, mf.imfasfmultiplexer_initialize, wmcontainer/IMFASFMultiplexer::Initialize
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
 - IMFASFMultiplexer::Initialize
 - wmcontainer/IMFASFMultiplexer::Initialize
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
 - IMFASFMultiplexer.Initialize
---

# IMFASFMultiplexer::Initialize


## -description

Initializes the multiplexer with the data from an ASF ContentInfo object.

## -parameters

### -param pIContentInfo [in]

Pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a> interface of the <b>MFASFContentInfo</b> object that contains the header information of the new ASF file. The multiplexer will generate data packets for this file.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>

## -remarks

This call must be made once at the beginning of encoding, with <i>pIContentInfo</i> pointing to the ASF ContentInfo object that describes the content to be encoded. This enables the ASF multiplexer to see, among other things, which streams will be present in the encoding session. This call typically does not affect the data in the ASF ContentInfo object.

## -see-also

<a href="/windows/desktop/medfound/creating-the-multiplexer-object">Creating the Multiplexer Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer">IMFASFMultiplexer</a>
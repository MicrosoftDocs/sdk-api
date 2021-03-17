---
UID: NF:wmcontainer.IMFASFMultiplexer.SetFlags
title: IMFASFMultiplexer::SetFlags (wmcontainer.h)
description: Sets multiplexer options.
helpviewer_keywords: ["IMFASFMultiplexer interface [Media Foundation]","SetFlags method","IMFASFMultiplexer.SetFlags","IMFASFMultiplexer::SetFlags","SetFlags","SetFlags method [Media Foundation]","SetFlags method [Media Foundation]","IMFASFMultiplexer interface","dac4f9b0-e83a-4e99-9a4a-ec1154c929a7","mf.imfasfmultiplexer_setflags","wmcontainer/IMFASFMultiplexer::SetFlags"]
old-location: mf\imfasfmultiplexer_setflags.htm
tech.root: mf
ms.assetid: dac4f9b0-e83a-4e99-9a4a-ec1154c929a7
ms.date: 12/05/2018
ms.keywords: IMFASFMultiplexer interface [Media Foundation],SetFlags method, IMFASFMultiplexer.SetFlags, IMFASFMultiplexer::SetFlags, SetFlags, SetFlags method [Media Foundation], SetFlags method [Media Foundation],IMFASFMultiplexer interface, dac4f9b0-e83a-4e99-9a4a-ec1154c929a7, mf.imfasfmultiplexer_setflags, wmcontainer/IMFASFMultiplexer::SetFlags
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
 - IMFASFMultiplexer::SetFlags
 - wmcontainer/IMFASFMultiplexer::SetFlags
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
 - IMFASFMultiplexer.SetFlags
---

# IMFASFMultiplexer::SetFlags


## -description

Sets multiplexer options.

## -parameters

### -param dwFlags [in]

Bitwise <b>OR</b> of zero or more members of the <a href="/windows/desktop/api/wmcontainer/ne-wmcontainer-mfasf_multiplexerflags">MFASF_MULTIPLEXERFLAGS</a> enumeration. These flags specify which multiplexer options to use. For more information, see "Multiplexer Initialization and Leaky Bucket Settings" in <a href="/windows/desktop/medfound/creating-the-multiplexer-object">Creating the Multiplexer Object</a>.

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

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer">IMFASFMultiplexer</a>
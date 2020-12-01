---
UID: NF:wmcontainer.IMFASFMultiplexer.GetFlags
title: IMFASFMultiplexer::GetFlags (wmcontainer.h)
description: Retrieves flags indicating the configured multiplexer options.
helpviewer_keywords: ["GetFlags","GetFlags method [Media Foundation]","GetFlags method [Media Foundation]","IMFASFMultiplexer interface","IMFASFMultiplexer interface [Media Foundation]","GetFlags method","IMFASFMultiplexer.GetFlags","IMFASFMultiplexer::GetFlags","b0aeefb5-6996-4abb-b869-855aaa7fcde2","mf.imfasfmultiplexer_getflags","wmcontainer/IMFASFMultiplexer::GetFlags"]
old-location: mf\imfasfmultiplexer_getflags.htm
tech.root: mf
ms.assetid: b0aeefb5-6996-4abb-b869-855aaa7fcde2
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Media Foundation], GetFlags method [Media Foundation],IMFASFMultiplexer interface, IMFASFMultiplexer interface [Media Foundation],GetFlags method, IMFASFMultiplexer.GetFlags, IMFASFMultiplexer::GetFlags, b0aeefb5-6996-4abb-b869-855aaa7fcde2, mf.imfasfmultiplexer_getflags, wmcontainer/IMFASFMultiplexer::GetFlags
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
 - IMFASFMultiplexer::GetFlags
 - wmcontainer/IMFASFMultiplexer::GetFlags
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
 - IMFASFMultiplexer.GetFlags
---

# IMFASFMultiplexer::GetFlags


## -description

Retrieves flags indicating the configured multiplexer options.

## -parameters

### -param pdwFlags [out]

Receives a bitwise <b>OR</b> of zero or more values from the <a href="/windows/desktop/api/wmcontainer/ne-wmcontainer-mfasf_multiplexerflags">MFASF_MULTIPLEXERFLAGS</a> enumeration. To set these flags, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags">IMFASFMultiplexer::SetFlags</a>.

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

<a href="/windows/desktop/medfound/creating-the-multiplexer-object">Creating the Multiplexer Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer">IMFASFMultiplexer</a>
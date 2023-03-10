---
UID: NF:mfidl.IMFTrustedOutput.IsFinal
title: IMFTrustedOutput::IsFinal (mfidl.h)
description: Queries whether this output is a policy sink, meaning it handles the rights and restrictions required by the input trust authority (ITA).
helpviewer_keywords: ["085cac9c-f8c1-45b9-a8fe-c2c5cc941439","IMFTrustedOutput interface [Media Foundation]","IsFinal method","IMFTrustedOutput.IsFinal","IMFTrustedOutput::IsFinal","IsFinal","IsFinal method [Media Foundation]","IsFinal method [Media Foundation]","IMFTrustedOutput interface","mf.imftrustedoutput_isfinal","mfidl/IMFTrustedOutput::IsFinal"]
old-location: mf\imftrustedoutput_isfinal.htm
tech.root: mf
ms.assetid: 085cac9c-f8c1-45b9-a8fe-c2c5cc941439
ms.date: 12/05/2018
ms.keywords: 085cac9c-f8c1-45b9-a8fe-c2c5cc941439, IMFTrustedOutput interface [Media Foundation],IsFinal method, IMFTrustedOutput.IsFinal, IMFTrustedOutput::IsFinal, IsFinal, IsFinal method [Media Foundation], IsFinal method [Media Foundation],IMFTrustedOutput interface, mf.imftrustedoutput_isfinal, mfidl/IMFTrustedOutput::IsFinal
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFTrustedOutput::IsFinal
 - mfidl/IMFTrustedOutput::IsFinal
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
 - IMFTrustedOutput.IsFinal
---

# IMFTrustedOutput::IsFinal


## -description

Queries whether this output is a policy sink, meaning it handles the rights and restrictions required by the input trust authority (ITA).

## -parameters

### -param pfIsFinal [out]

Receives a Boolean value. If <b>TRUE</b>, this object is a policy sink. If <b>FALSE</b>, the policy must be enforced further downstream.

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

A trusted output is generally considered to be a policy sink if it does not pass the media content that it receives anywhere else; or, if it does pass the media content elsewhere, either it protects the content using some proprietary method such as encryption, or it sufficiently devalues the content so as not to require protection.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput">IMFTrustedOutput</a>
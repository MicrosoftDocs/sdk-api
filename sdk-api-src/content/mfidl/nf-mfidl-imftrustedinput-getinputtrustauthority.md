---
UID: NF:mfidl.IMFTrustedInput.GetInputTrustAuthority
title: IMFTrustedInput::GetInputTrustAuthority (mfidl.h)
description: Retrieves the input trust authority (ITA) for a specified stream.
helpviewer_keywords: ["GetInputTrustAuthority","GetInputTrustAuthority method [Media Foundation]","GetInputTrustAuthority method [Media Foundation]","IMFTrustedInput interface","IMFTrustedInput interface [Media Foundation]","GetInputTrustAuthority method","IMFTrustedInput.GetInputTrustAuthority","IMFTrustedInput::GetInputTrustAuthority","b4ebf02e-554a-4e7e-93d3-6f37d8b689bf","mf.imftrustedinput_getinputtrustauthority","mfidl/IMFTrustedInput::GetInputTrustAuthority"]
old-location: mf\imftrustedinput_getinputtrustauthority.htm
tech.root: mf
ms.assetid: b4ebf02e-554a-4e7e-93d3-6f37d8b689bf
ms.date: 12/05/2018
ms.keywords: GetInputTrustAuthority, GetInputTrustAuthority method [Media Foundation], GetInputTrustAuthority method [Media Foundation],IMFTrustedInput interface, IMFTrustedInput interface [Media Foundation],GetInputTrustAuthority method, IMFTrustedInput.GetInputTrustAuthority, IMFTrustedInput::GetInputTrustAuthority, b4ebf02e-554a-4e7e-93d3-6f37d8b689bf, mf.imftrustedinput_getinputtrustauthority, mfidl/IMFTrustedInput::GetInputTrustAuthority
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
 - IMFTrustedInput::GetInputTrustAuthority
 - mfidl/IMFTrustedInput::GetInputTrustAuthority
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
 - IMFTrustedInput.GetInputTrustAuthority
---

# IMFTrustedInput::GetInputTrustAuthority


## -description

Retrieves the input trust authority (ITA) for a specified stream.  If the specified stream is not protected, this method must return MF_E_NOT_PROTECTED.

## -parameters

### -param dwStreamID [in]

The stream identifier for which the ITA is being requested.

### -param riid [in]

The interface identifier (IID) of the interface being requested. Currently the only supported value is IID_IMFInputTrustAuthority.

### -param ppunkObject [out]

Receives a pointer to the ITA's <b>IUnknown</b> interface. The caller must release the interface.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The ITA does not expose the requested interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
The specified stream is not protected.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority">IMFInputTrustAuthority</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput">IMFTrustedInput</a>

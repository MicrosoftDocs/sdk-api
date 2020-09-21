---
UID: NF:mfidl.IMFInputTrustAuthority.GetPolicy
title: IMFInputTrustAuthority::GetPolicy (mfidl.h)
description: Retrieves the policy that defines which output protection systems are allowed for this stream, and the configuration data for each protection system.
helpviewer_keywords: ["4d840b56-47e0-4c2f-b2e7-a17586dad8d1","GetPolicy","GetPolicy method [Media Foundation]","GetPolicy method [Media Foundation]","IMFInputTrustAuthority interface","IMFInputTrustAuthority interface [Media Foundation]","GetPolicy method","IMFInputTrustAuthority.GetPolicy","IMFInputTrustAuthority::GetPolicy","mf.imfinputtrustauthority_getpolicy","mfidl/IMFInputTrustAuthority::GetPolicy"]
old-location: mf\imfinputtrustauthority_getpolicy.htm
tech.root: mf
ms.assetid: 4d840b56-47e0-4c2f-b2e7-a17586dad8d1
ms.date: 12/05/2018
ms.keywords: 4d840b56-47e0-4c2f-b2e7-a17586dad8d1, GetPolicy, GetPolicy method [Media Foundation], GetPolicy method [Media Foundation],IMFInputTrustAuthority interface, IMFInputTrustAuthority interface [Media Foundation],GetPolicy method, IMFInputTrustAuthority.GetPolicy, IMFInputTrustAuthority::GetPolicy, mf.imfinputtrustauthority_getpolicy, mfidl/IMFInputTrustAuthority::GetPolicy
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
 - IMFInputTrustAuthority::GetPolicy
 - mfidl/IMFInputTrustAuthority::GetPolicy
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
 - IMFInputTrustAuthority.GetPolicy
---

# IMFInputTrustAuthority::GetPolicy


## -description

Retrieves the policy that defines which output protection systems are allowed for this stream, and the configuration data for each protection system.

## -parameters

### -param Action [in]

The action that will be performed on this stream, specified as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfpolicymanager_action">MFPOLICYMANAGER_ACTION</a> enumeration.

### -param ppPolicy [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy">IMFOutputPolicy</a> interface. The caller must release the interface.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority">IMFInputTrustAuthority</a>
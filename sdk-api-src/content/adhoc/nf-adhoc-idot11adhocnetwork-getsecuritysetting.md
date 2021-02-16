---
UID: NF:adhoc.IDot11AdHocNetwork.GetSecuritySetting
title: IDot11AdHocNetwork::GetSecuritySetting (adhoc.h)
description: Gets the security settings for the network.
helpviewer_keywords: ["GetSecuritySetting","GetSecuritySetting method [NativeWIFI]","GetSecuritySetting method [NativeWIFI]","IDot11AdHocNetwork interface","IDot11AdHocNetwork interface [NativeWIFI]","GetSecuritySetting method","IDot11AdHocNetwork.GetSecuritySetting","IDot11AdHocNetwork::GetSecuritySetting","adhoc/IDot11AdHocNetwork::GetSecuritySetting","nwifi.idot11adhocnetwork_getsecuritysetting"]
old-location: nwifi\idot11adhocnetwork_getsecuritysetting.htm
tech.root: nwifi
ms.assetid: 3e5fa757-41fd-4541-a16e-15c2fb66e15a
ms.date: 12/05/2018
ms.keywords: GetSecuritySetting, GetSecuritySetting method [NativeWIFI], GetSecuritySetting method [NativeWIFI],IDot11AdHocNetwork interface, IDot11AdHocNetwork interface [NativeWIFI],GetSecuritySetting method, IDot11AdHocNetwork.GetSecuritySetting, IDot11AdHocNetwork::GetSecuritySetting, adhoc/IDot11AdHocNetwork::GetSecuritySetting, nwifi.idot11adhocnetwork_getsecuritysetting
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
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
 - IDot11AdHocNetwork::GetSecuritySetting
 - adhoc/IDot11AdHocNetwork::GetSecuritySetting
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocNetwork.GetSecuritySetting
---

# IDot11AdHocNetwork::GetSecuritySetting


## -description

Gets the security settings for the network.

## -parameters

### -param pAdHocSecuritySetting [out]

A pointer to an <a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings">IDot11AdHocSecuritySettings</a> interface that contains the security settings for the network.

## -returns

Possible return values include, but are not limited to, the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a>
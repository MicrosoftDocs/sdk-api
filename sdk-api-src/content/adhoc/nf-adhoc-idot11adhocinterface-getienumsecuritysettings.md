---
UID: NF:adhoc.IDot11AdHocInterface.GetIEnumSecuritySettings
title: IDot11AdHocInterface::GetIEnumSecuritySettings (adhoc.h)
description: Gets the collection of security settings associated with this NIC.
helpviewer_keywords: ["GetIEnumSecuritySettings","GetIEnumSecuritySettings method [NativeWIFI]","GetIEnumSecuritySettings method [NativeWIFI]","IDot11AdHocInterface interface","IDot11AdHocInterface interface [NativeWIFI]","GetIEnumSecuritySettings method","IDot11AdHocInterface.GetIEnumSecuritySettings","IDot11AdHocInterface::GetIEnumSecuritySettings","adhoc/IDot11AdHocInterface::GetIEnumSecuritySettings","nwifi.idot11adhocinterface_getienumsecuritysettings"]
old-location: nwifi\idot11adhocinterface_getienumsecuritysettings.htm
tech.root: nwifi
ms.assetid: e5f98222-83aa-4ba9-adc7-e7b67eb5dc0d
ms.date: 12/05/2018
ms.keywords: GetIEnumSecuritySettings, GetIEnumSecuritySettings method [NativeWIFI], GetIEnumSecuritySettings method [NativeWIFI],IDot11AdHocInterface interface, IDot11AdHocInterface interface [NativeWIFI],GetIEnumSecuritySettings method, IDot11AdHocInterface.GetIEnumSecuritySettings, IDot11AdHocInterface::GetIEnumSecuritySettings, adhoc/IDot11AdHocInterface::GetIEnumSecuritySettings, nwifi.idot11adhocinterface_getienumsecuritysettings
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
 - IDot11AdHocInterface::GetIEnumSecuritySettings
 - adhoc/IDot11AdHocInterface::GetIEnumSecuritySettings
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
 - IDot11AdHocInterface.GetIEnumSecuritySettings
---

# IDot11AdHocInterface::GetIEnumSecuritySettings


## -description

Gets the collection of security settings associated with this NIC.

## -parameters

### -param ppEnum [out]

A pointer to an <a href="/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings">IEnumDot11AdHocSecuritySettings</a> interface that contains the collection of security settings.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface">IDot11AdHocInterface</a>
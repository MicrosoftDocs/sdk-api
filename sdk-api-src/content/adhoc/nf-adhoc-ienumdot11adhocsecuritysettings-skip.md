---
UID: NF:adhoc.IEnumDot11AdHocSecuritySettings.Skip
title: IEnumDot11AdHocSecuritySettings::Skip (adhoc.h)
description: Skips over the next specified number of elements in the enumeration sequence. (IEnumDot11AdHocSecuritySettings.Skip)
helpviewer_keywords: ["IEnumDot11AdHocSecuritySettings interface [NativeWIFI]","Skip method","IEnumDot11AdHocSecuritySettings.Skip","IEnumDot11AdHocSecuritySettings::Skip","Skip","Skip method [NativeWIFI]","Skip method [NativeWIFI]","IEnumDot11AdHocSecuritySettings interface","adhoc/IEnumDot11AdHocSecuritySettings::Skip","nwifi.ienumdot11adhocsecuritysettings_skip"]
old-location: nwifi\ienumdot11adhocsecuritysettings_skip.htm
tech.root: nwifi
ms.assetid: c423e794-bb3a-4dd8-b6bc-324d91909e92
ms.date: 12/05/2018
ms.keywords: IEnumDot11AdHocSecuritySettings interface [NativeWIFI],Skip method, IEnumDot11AdHocSecuritySettings.Skip, IEnumDot11AdHocSecuritySettings::Skip, Skip, Skip method [NativeWIFI], Skip method [NativeWIFI],IEnumDot11AdHocSecuritySettings interface, adhoc/IEnumDot11AdHocSecuritySettings::Skip, nwifi.ienumdot11adhocsecuritysettings_skip
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
 - IEnumDot11AdHocSecuritySettings::Skip
 - adhoc/IEnumDot11AdHocSecuritySettings::Skip
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
 - IEnumDot11AdHocSecuritySettings.Skip
---

# IEnumDot11AdHocSecuritySettings::Skip


## -description

Skips over the next specified number of elements in the enumeration sequence.

## -parameters

### -param cElt [in]

The number of elements to skip.

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
</table>

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings">IEnumDot11AdHocSecuritySettings</a>

---
UID: NF:adhoc.IDot11AdHocInterface.IsDot11d
title: IDot11AdHocInterface::IsDot11d (adhoc.h)
description: Specifies whether the NIC is 802.11d compliant.
helpviewer_keywords: ["IDot11AdHocInterface interface [NativeWIFI]","IsDot11d method","IDot11AdHocInterface.IsDot11d","IDot11AdHocInterface::IsDot11d","IsDot11d","IsDot11d method [NativeWIFI]","IsDot11d method [NativeWIFI]","IDot11AdHocInterface interface","adhoc/IDot11AdHocInterface::IsDot11d","nwifi.idot11adhocinterface_isdot11d"]
old-location: nwifi\idot11adhocinterface_isdot11d.htm
tech.root: nwifi
ms.assetid: 3854b2e3-853d-44cd-9b43-6c583f0df08f
ms.date: 12/05/2018
ms.keywords: IDot11AdHocInterface interface [NativeWIFI],IsDot11d method, IDot11AdHocInterface.IsDot11d, IDot11AdHocInterface::IsDot11d, IsDot11d, IsDot11d method [NativeWIFI], IsDot11d method [NativeWIFI],IDot11AdHocInterface interface, adhoc/IDot11AdHocInterface::IsDot11d, nwifi.idot11adhocinterface_isdot11d
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
 - IDot11AdHocInterface::IsDot11d
 - adhoc/IDot11AdHocInterface::IsDot11d
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
 - IDot11AdHocInterface.IsDot11d
---

# IDot11AdHocInterface::IsDot11d


## -description

Specifies whether the NIC is 802.11d compliant.

## -parameters

### -param pf11d [in, out]

A pointer to a boolean that specifies 802.11d compliance. The boolean value is set to <b>TRUE</b> if  the NIC is compliant and <b>FALSE</b> otherwise.

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

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface">IDot11AdHocInterface</a>
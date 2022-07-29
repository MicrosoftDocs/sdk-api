---
UID: NF:adhoc.IEnumDot11AdHocNetworks.Skip
title: IEnumDot11AdHocNetworks::Skip (adhoc.h)
description: Skips over the next specified number of elements in the enumeration sequence. (IEnumDot11AdHocNetworks.Skip)
helpviewer_keywords: ["IEnumDot11AdHocNetworks interface [NativeWIFI]","Skip method","IEnumDot11AdHocNetworks.Skip","IEnumDot11AdHocNetworks::Skip","Skip","Skip method [NativeWIFI]","Skip method [NativeWIFI]","IEnumDot11AdHocNetworks interface","adhoc/IEnumDot11AdHocNetworks::Skip","nwifi.ienumdot11adhocnetworks_skip"]
old-location: nwifi\ienumdot11adhocnetworks_skip.htm
tech.root: nwifi
ms.assetid: 31e182f8-6a19-4138-b799-7ad485868d19
ms.date: 12/05/2018
ms.keywords: IEnumDot11AdHocNetworks interface [NativeWIFI],Skip method, IEnumDot11AdHocNetworks.Skip, IEnumDot11AdHocNetworks::Skip, Skip, Skip method [NativeWIFI], Skip method [NativeWIFI],IEnumDot11AdHocNetworks interface, adhoc/IEnumDot11AdHocNetworks::Skip, nwifi.ienumdot11adhocnetworks_skip
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
 - IEnumDot11AdHocNetworks::Skip
 - adhoc/IEnumDot11AdHocNetworks::Skip
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
 - IEnumDot11AdHocNetworks.Skip
---

# IEnumDot11AdHocNetworks::Skip


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

<a href="/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks">IEnumDot11AdHocNetworks</a>

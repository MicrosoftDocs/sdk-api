---
UID: NF:adhoc.IDot11AdHocNetwork.GetSignalQuality
title: IDot11AdHocNetwork::GetSignalQuality (adhoc.h)
description: Gets the signal quality values associated with the network's radio.
helpviewer_keywords: ["GetSignalQuality","GetSignalQuality method [NativeWIFI]","GetSignalQuality method [NativeWIFI]","IDot11AdHocNetwork interface","IDot11AdHocNetwork interface [NativeWIFI]","GetSignalQuality method","IDot11AdHocNetwork.GetSignalQuality","IDot11AdHocNetwork::GetSignalQuality","adhoc/IDot11AdHocNetwork::GetSignalQuality","nwifi.idot11adhocnetwork_getsignalquality"]
old-location: nwifi\idot11adhocnetwork_getsignalquality.htm
tech.root: nwifi
ms.assetid: be31a2ed-c9ba-4894-a295-a88e01639891
ms.date: 12/05/2018
ms.keywords: GetSignalQuality, GetSignalQuality method [NativeWIFI], GetSignalQuality method [NativeWIFI],IDot11AdHocNetwork interface, IDot11AdHocNetwork interface [NativeWIFI],GetSignalQuality method, IDot11AdHocNetwork.GetSignalQuality, IDot11AdHocNetwork::GetSignalQuality, adhoc/IDot11AdHocNetwork::GetSignalQuality, nwifi.idot11adhocnetwork_getsignalquality
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
 - IDot11AdHocNetwork::GetSignalQuality
 - adhoc/IDot11AdHocNetwork::GetSignalQuality
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
 - IDot11AdHocNetwork.GetSignalQuality
---

# IDot11AdHocNetwork::GetSignalQuality


## -description

Gets the signal quality values associated with the network's radio.

## -parameters

### -param puStrengthValue [out]

The current signal strength. This parameter takes a ULONG value between 0 and <i>puStrengthMax</i>.

### -param puStrengthMax [out]

The maximum signal strength value. This parameter takes a ULONG value between 0 and 100. By default, <i>puStrengthMax</i> is set to 100.

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

## -remarks

Signal strength, in this context, is measured on a linear scale. When <i>puStrengthMax</i> is set to the default value of 100, <i>puStrengthValue</i> represents the  percentage of the maximum signal strength currently used for transmission.

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork">IDot11AdHocNetwork</a>
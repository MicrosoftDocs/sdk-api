---
UID: NF:adhoc.IDot11AdHocInterface.IsRadioOn
title: IDot11AdHocInterface::IsRadioOn (adhoc.h)
description: Specifies whether the radio is on.
helpviewer_keywords: ["IDot11AdHocInterface interface [NativeWIFI]","IsRadioOn method","IDot11AdHocInterface.IsRadioOn","IDot11AdHocInterface::IsRadioOn","IsRadioOn","IsRadioOn method [NativeWIFI]","IsRadioOn method [NativeWIFI]","IDot11AdHocInterface interface","adhoc/IDot11AdHocInterface::IsRadioOn","nwifi.idot11adhocinterface_isradioon"]
old-location: nwifi\idot11adhocinterface_isradioon.htm
tech.root: nwifi
ms.assetid: f5d76166-b960-4b70-acf7-e8eb65ca8cfb
ms.date: 12/05/2018
ms.keywords: IDot11AdHocInterface interface [NativeWIFI],IsRadioOn method, IDot11AdHocInterface.IsRadioOn, IDot11AdHocInterface::IsRadioOn, IsRadioOn, IsRadioOn method [NativeWIFI], IsRadioOn method [NativeWIFI],IDot11AdHocInterface interface, adhoc/IDot11AdHocInterface::IsRadioOn, nwifi.idot11adhocinterface_isradioon
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
 - IDot11AdHocInterface::IsRadioOn
 - adhoc/IDot11AdHocInterface::IsRadioOn
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
 - IDot11AdHocInterface.IsRadioOn
---

# IDot11AdHocInterface::IsRadioOn


## -description

Specifies whether the radio is on.

## -parameters

### -param pfIsRadioOn [in, out]

A pointer to a boolean that specifies the radio state. The value is set to <b>TRUE</b> if the radio is on.

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
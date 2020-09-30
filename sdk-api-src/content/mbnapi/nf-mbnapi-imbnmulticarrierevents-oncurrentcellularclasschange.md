---
UID: NF:mbnapi.IMbnMultiCarrierEvents.OnCurrentCellularClassChange
title: IMbnMultiCarrierEvents::OnCurrentCellularClassChange (mbnapi.h)
description: This notification method is called by the Mobile Broadband service to indicate the completion of a GetCurrentCellularClass operation.
helpviewer_keywords: ["IMbnMultiCarrierEvents interface [Microsoft Broadband Networks]","OnCurrentCellularClassChange method","IMbnMultiCarrierEvents.OnCurrentCellularClassChange","IMbnMultiCarrierEvents::OnCurrentCellularClassChange","OnCurrentCellularClassChange","OnCurrentCellularClassChange method [Microsoft Broadband Networks]","OnCurrentCellularClassChange method [Microsoft Broadband Networks]","IMbnMultiCarrierEvents interface","mbn.imbnmulticarrierevents_oncurrentcellularclasschange","mbnapi/IMbnMultiCarrierEvents::OnCurrentCellularClassChange"]
old-location: mbn\imbnmulticarrierevents_oncurrentcellularclasschange.htm
tech.root: mbn
ms.assetid: 76B5349E-EA51-422D-81BC-A93B85FBCF90
ms.date: 12/05/2018
ms.keywords: IMbnMultiCarrierEvents interface [Microsoft Broadband Networks],OnCurrentCellularClassChange method, IMbnMultiCarrierEvents.OnCurrentCellularClassChange, IMbnMultiCarrierEvents::OnCurrentCellularClassChange, OnCurrentCellularClassChange, OnCurrentCellularClassChange method [Microsoft Broadband Networks], OnCurrentCellularClassChange method [Microsoft Broadband Networks],IMbnMultiCarrierEvents interface, mbn.imbnmulticarrierevents_oncurrentcellularclasschange, mbnapi/IMbnMultiCarrierEvents::OnCurrentCellularClassChange
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnMultiCarrierEvents::OnCurrentCellularClassChange
 - mbnapi/IMbnMultiCarrierEvents::OnCurrentCellularClassChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnMultiCarrierEvents.OnCurrentCellularClassChange
---

# IMbnMultiCarrierEvents::OnCurrentCellularClassChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-getcurrentcellularclass">GetCurrentCellularClass</a> operation.

## -parameters

### -param mbnInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a> object that represents the Mobile Broadband device <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-getcurrentcellularclass">GetCurrentCellularClass</a> operation.

## -returns

This method can return one of these values.

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
The operation  was successful.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrierevents">IMbnMultiCarrierEvents</a>
---
UID: NC:winbio_adapter.PIBIO_STORAGE_QUERY_EXTENDED_INFO_FN
title: PIBIO_STORAGE_QUERY_EXTENDED_INFO_FN (winbio_adapter.h)
description: Determines the capabilities and limitations of the biometric storage component.
helpviewer_keywords: ["PIBIO_STORAGE_QUERY_EXTENDED_INFO_FN","PIBIO_STORAGE_QUERY_EXTENDED_INFO_FN callback","StorageAdapterQueryExtendedInfo","StorageAdapterQueryExtendedInfo callback function [Windows Biometric Framework API]","secbiomet.storageadapterqueryextendedinfo","winbio_adapter/StorageAdapterQueryExtendedInfo"]
old-location: secbiomet\storageadapterqueryextendedinfo.htm
tech.root: SecBioMet
ms.assetid: BCA55006-73F4-4845-84B3-34A6255D673F
ms.date: 12/05/2018
ms.keywords: PIBIO_STORAGE_QUERY_EXTENDED_INFO_FN, PIBIO_STORAGE_QUERY_EXTENDED_INFO_FN callback, StorageAdapterQueryExtendedInfo, StorageAdapterQueryExtendedInfo callback function [Windows Biometric Framework API], secbiomet.storageadapterqueryextendedinfo, winbio_adapter/StorageAdapterQueryExtendedInfo
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - PIBIO_STORAGE_QUERY_EXTENDED_INFO_FN
 - winbio_adapter/PIBIO_STORAGE_QUERY_EXTENDED_INFO_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - StorageAdapterQueryExtendedInfo
---

# PIBIO_STORAGE_QUERY_EXTENDED_INFO_FN callback function


## -description

Called by the Windows Biometric Framework to determine the capabilities and limitations of the biometric storage component.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param StorageInfo [out]

Pointer to the <a href="/windows/desktop/SecBioMet/winbio-extended-storage-info">WINBIO_EXTENDED_STORAGE_INFO</a> structure that contains the storage information returned by this function.

### -param StorageInfoSize [in]

The specified size of the storage information.

## -returns

If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> and <i>StorageInfo</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
The <i>StorageInfoSize</i> value is less than the size needed to return the storage information.

</td>
</tr>
</table>

## -remarks

This method is called once during configuration of the biometric unit. 

It will also be called if a client application uses the <a href="/windows/desktop/api/winbio/nf-winbio-winbiogetproperty">WinBioGetProperty</a> function to query the value of the <b>WINBIO_PROPERTY_EXTENDED_STORAGE_INFO</b> property.
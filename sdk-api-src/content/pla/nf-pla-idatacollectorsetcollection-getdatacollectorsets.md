---
UID: NF:pla.IDataCollectorSetCollection.GetDataCollectorSets
title: IDataCollectorSetCollection::GetDataCollectorSets (pla.h)
description: Populates the data collector set collection.
helpviewer_keywords: ["GetDataCollectorSets","GetDataCollectorSets method [PLA]","GetDataCollectorSets method [PLA]","IDataCollectorSetCollection interface","IDataCollectorSetCollection interface [PLA]","GetDataCollectorSets method","IDataCollectorSetCollection.GetDataCollectorSets","IDataCollectorSetCollection::GetDataCollectorSets","base.idatacollectorsetcollection_getdatacollectorsets","pla.idatacollectorsetcollection_getdatacollectorsets","pla/IDataCollectorSetCollection::GetDataCollectorSets"]
old-location: pla\idatacollectorsetcollection_getdatacollectorsets.htm
tech.root: PLA
ms.assetid: 190c96ad-6193-4f74-906f-180575e6e418
ms.date: 12/05/2018
ms.keywords: GetDataCollectorSets, GetDataCollectorSets method [PLA], GetDataCollectorSets method [PLA],IDataCollectorSetCollection interface, IDataCollectorSetCollection interface [PLA],GetDataCollectorSets method, IDataCollectorSetCollection.GetDataCollectorSets, IDataCollectorSetCollection::GetDataCollectorSets, base.idatacollectorsetcollection_getdatacollectorsets, pla.idatacollectorsetcollection_getdatacollectorsets, pla/IDataCollectorSetCollection::GetDataCollectorSets
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataCollectorSetCollection::GetDataCollectorSets
 - pla/IDataCollectorSetCollection::GetDataCollectorSets
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSetCollection.GetDataCollectorSets
---

# IDataCollectorSetCollection::GetDataCollectorSets


## -description

Populates the data collector set collection.

## -parameters

### -param server [in]

The computer whose data collector sets you want to enumerate. You can specify a computer name, a fully qualified domain name, or an IP address (IPv4 or IPv6 format). If <b>NULL</b>, PLA enumerates the sets on the local computer.

### -param filter [in]

If empty, PLA enumerates sets from all namespaces; otherwise, specify a specific namespace to enumerate. The form is &lt;namespace&gt;\*. For possible namespace values, see <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">IDataCollectorSet::Commit</a>.

## -returns

Returns S_OK if successful. The following table shows possible error values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)</b></dt>
</dl>
</td>
<td width="60%">
The RPC server is not available. The method is unable to query the data collector set remotely. To query the data collector set from a remote computer running Windows Vista, enable Performance Logs and Alerts in <b>Windows Firewall Settings</b> on the remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_BAD_NETPATH)</b></dt>
</dl>
</td>
<td width="60%">
Unable to find the remote computer.

</td>
</tr>
</table>

## -remarks

The method enumerates only those sets that have been previously saved using <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">IDataCollectorSet::Commit</a>.

 The retrieved data collector sets overwrite the contents of this instance. The instance must be empty (newly created) or be from the same namespace.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorsetcollection">IDataCollectorSetCollection</a>
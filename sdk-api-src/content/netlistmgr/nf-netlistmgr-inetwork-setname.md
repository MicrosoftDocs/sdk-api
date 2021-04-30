---
UID: NF:netlistmgr.INetwork.SetName
title: INetwork::SetName (netlistmgr.h)
description: The SetName method sets or renames a network.
helpviewer_keywords: ["INetwork interface [Network Awareness]","SetName method","INetwork.SetName","INetwork::SetName","SetName","SetName method [Network Awareness]","SetName method [Network Awareness]","INetwork interface","netlistmgr/INetwork::SetName","nla.inetwork_setname"]
old-location: nla\inetwork_setname.htm
tech.root: nla
ms.assetid: 7495e26f-b7cf-4abd-ab7d-82b0d4bd4d87
ms.date: 12/05/2018
ms.keywords: INetwork interface [Network Awareness],SetName method, INetwork.SetName, INetwork::SetName, SetName, SetName method [Network Awareness], SetName method [Network Awareness],INetwork interface, netlistmgr/INetwork::SetName, nla.inetwork_setname
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
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
 - INetwork::SetName
 - netlistmgr/INetwork::SetName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetwork.SetName
---

# INetwork::SetName


## -description

The <b>SetName</b> method sets or renames a network.

## -parameters

### -param szNetworkNewName [in]

Zero-terminated string that contains the new name of the network.

## -returns

Returns S_OK if the method succeeds. Otherwise, the method returns one of the following values.

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
<i>szNetworkNewName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILENAME_EXCED_RANGE)</b></dt>
</dl>
</td>
<td width="60%">
The name provided is too long. 

</td>
</tr>
</table>

## -remarks

The maximum length of a network name can be 128 characters and cannot contain spaces only, tab or "\ /: * ? " &lt; &gt; |".

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a>
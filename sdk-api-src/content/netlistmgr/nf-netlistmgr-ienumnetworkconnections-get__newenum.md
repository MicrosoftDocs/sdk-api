---
UID: NF:netlistmgr.IEnumNetworkConnections.get__NewEnum
title: IEnumNetworkConnections::get__NewEnum (netlistmgr.h)
description: The get_NewEnum property returns an automation enumerator object that you can use to iterate through the IEnumNetworkConnections collection.
helpviewer_keywords: ["IEnumNetworkConnections interface [Network Awareness]","get__NewEnum method","IEnumNetworkConnections.get__NewEnum","IEnumNetworkConnections::get__NewEnum","get__NewEnum","get__NewEnum method [Network Awareness]","get__NewEnum method [Network Awareness]","IEnumNetworkConnections interface","netlistmgr/IEnumNetworkConnections::get__NewEnum","nla.ienumnetworkconnections_get__newenum"]
old-location: nla\ienumnetworkconnections_get__newenum.htm
tech.root: nla
ms.assetid: 38b3a58e-6ed1-488e-b5b8-50043adae8cc
ms.date: 12/05/2018
ms.keywords: IEnumNetworkConnections interface [Network Awareness],get__NewEnum method, IEnumNetworkConnections.get__NewEnum, IEnumNetworkConnections::get__NewEnum, get__NewEnum, get__NewEnum method [Network Awareness], get__NewEnum method [Network Awareness],IEnumNetworkConnections interface, netlistmgr/IEnumNetworkConnections::get__NewEnum, nla.ienumnetworkconnections_get__newenum
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
 - IEnumNetworkConnections::get__NewEnum
 - netlistmgr/IEnumNetworkConnections::get__NewEnum
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
 - IEnumNetworkConnections.get__NewEnum
---

# IEnumNetworkConnections::get__NewEnum


## -description

The <b>get_NewEnum</b> property returns an automation enumerator object that you can use to iterate through the <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworkconnections">IEnumNetworkConnections</a> collection.

## -parameters

### -param ppEnumVar [out]

Contains the new instance of the implemented interface.

## -returns

Returns S_OK if the method succeeds.

## -remarks

In Microsoft Visual Basic and Microsoft C#, you do not need to use the corresponding _NewEnum property, because it is automatically used in the implementation of  the For Each loop (for each in Visual C#).

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworkconnections">IEnumNetworkConnections</a>
---
UID: NF:netlistmgr.IEnumNetworks.get__NewEnum
title: IEnumNetworks::get__NewEnum (netlistmgr.h)
description: The get_NewEnum property returns an automation enumerator object that you can use to iterate through the IEnumNetworks collection.
helpviewer_keywords: ["IEnumNetworks interface [Network Awareness]","get__NewEnum method","IEnumNetworks.get__NewEnum","IEnumNetworks::get__NewEnum","get__NewEnum","get__NewEnum method [Network Awareness]","get__NewEnum method [Network Awareness]","IEnumNetworks interface","netlistmgr/IEnumNetworks::get__NewEnum","nla.ienumnetworks_get__newenum"]
old-location: nla\ienumnetworks_get__newenum.htm
tech.root: nla
ms.assetid: ddff98c2-669d-4f8d-9584-b8590705c2f0
ms.date: 12/05/2018
ms.keywords: IEnumNetworks interface [Network Awareness],get__NewEnum method, IEnumNetworks.get__NewEnum, IEnumNetworks::get__NewEnum, get__NewEnum, get__NewEnum method [Network Awareness], get__NewEnum method [Network Awareness],IEnumNetworks interface, netlistmgr/IEnumNetworks::get__NewEnum, nla.ienumnetworks_get__newenum
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
 - IEnumNetworks::get__NewEnum
 - netlistmgr/IEnumNetworks::get__NewEnum
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
 - IEnumNetworks.get__NewEnum
---

# IEnumNetworks::get__NewEnum


## -description

The <b>get_NewEnum</b> property returns an automation enumerator object that you can use to iterate through the <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworks">IEnumNetworks</a> collection.

## -parameters

### -param ppEnumVar [out]

Contains the new instance of the implemented interface.

## -returns

Returns S_OK if the method succeeds.

## -remarks

In Microsoft Visual Basic and Microsoft C#, you do not need to use the corresponding _NewEnum property, because it is automatically used in the implementation of  the For Each loop (for each in Visual C#).

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworks">IEnumNetworks</a>
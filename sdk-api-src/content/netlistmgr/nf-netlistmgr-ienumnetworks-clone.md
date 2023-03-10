---
UID: NF:netlistmgr.IEnumNetworks.Clone
title: IEnumNetworks::Clone (netlistmgr.h)
description: The Clone method creates an enumerator that contains the same enumeration state as the enumerator currently in use. (IEnumNetworks.Clone)
helpviewer_keywords: ["Clone","Clone method [Network Awareness]","Clone method [Network Awareness]","IEnumNetworks interface","IEnumNetworks interface [Network Awareness]","Clone method","IEnumNetworks.Clone","IEnumNetworks::Clone","netlistmgr/IEnumNetworks::Clone","nla.ienumnetworks_clone"]
old-location: nla\ienumnetworks_clone.htm
tech.root: nla
ms.assetid: 196bf9fa-4615-44c3-accf-f70516d5a6a5
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Network Awareness], Clone method [Network Awareness],IEnumNetworks interface, IEnumNetworks interface [Network Awareness],Clone method, IEnumNetworks.Clone, IEnumNetworks::Clone, netlistmgr/IEnumNetworks::Clone, nla.ienumnetworks_clone
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
 - IEnumNetworks::Clone
 - netlistmgr/IEnumNetworks::Clone
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
 - IEnumNetworks.Clone
---

# IEnumNetworks::Clone


## -description

The <b>Clone</b> method creates an enumerator that contains the same enumeration state as the enumerator currently in use.

## -parameters

### -param ppEnumNetwork [out]

Pointer to a new <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworks">IEnumNetworks</a> interface.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworks">IEnumNetworks</a>

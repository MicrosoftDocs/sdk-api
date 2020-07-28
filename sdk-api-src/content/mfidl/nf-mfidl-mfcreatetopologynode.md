---
UID: NF:mfidl.MFCreateTopologyNode
title: MFCreateTopologyNode function (mfidl.h)
description: Creates a topology node.
helpviewer_keywords: ["67c32232-09cb-4098-b80b-4b93ee121190","MFCreateTopologyNode","MFCreateTopologyNode function [Media Foundation]","mf.mfcreatetopologynode","mfidl/MFCreateTopologyNode"]
old-location: mf\mfcreatetopologynode.htm
tech.root: mf
ms.assetid: 67c32232-09cb-4098-b80b-4b93ee121190
ms.date: 12/05/2018
ms.keywords: 67c32232-09cb-4098-b80b-4b93ee121190, MFCreateTopologyNode, MFCreateTopologyNode function [Media Foundation], mf.mfcreatetopologynode, mfidl/MFCreateTopologyNode
f1_keywords:
- mfidl/MFCreateTopologyNode
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mf.dll
api_name:
- MFCreateTopologyNode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateTopologyNode function


## -description


Creates a topology node.


## -parameters




### -param NodeType [in]

The type of node to create, specified as a member of the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/ne-mfidl-mf_topology_type">MF_TOPOLOGY_TYPE</a> enumeration.


### -param ppNode [out]

Receives a pointer to the node's <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/creating-output-nodes">Creating Output Nodes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/creating-source-nodes">Creating Source Nodes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/creating-transform-nodes">Creating Transform Nodes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topologies">Topologies</a>
 

 


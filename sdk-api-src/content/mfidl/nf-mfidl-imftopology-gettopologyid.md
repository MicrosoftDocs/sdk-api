---
UID: NF:mfidl.IMFTopology.GetTopologyID
title: IMFTopology::GetTopologyID (mfidl.h)
description: Gets the identifier of the topology.
helpviewer_keywords: ["GetTopologyID","GetTopologyID method [Media Foundation]","GetTopologyID method [Media Foundation]","IMFTopology interface","IMFTopology interface [Media Foundation]","GetTopologyID method","IMFTopology.GetTopologyID","IMFTopology::GetTopologyID","f7d33d20-1b58-4b88-9a98-1004a5c42dfa","mf.imftopology_gettopologyid","mfidl/IMFTopology::GetTopologyID"]
old-location: mf\imftopology_gettopologyid.htm
tech.root: mf
ms.assetid: f7d33d20-1b58-4b88-9a98-1004a5c42dfa
ms.date: 12/05/2018
ms.keywords: GetTopologyID, GetTopologyID method [Media Foundation], GetTopologyID method [Media Foundation],IMFTopology interface, IMFTopology interface [Media Foundation],GetTopologyID method, IMFTopology.GetTopologyID, IMFTopology::GetTopologyID, f7d33d20-1b58-4b88-9a98-1004a5c42dfa, mf.imftopology_gettopologyid, mfidl/IMFTopology::GetTopologyID
f1_keywords:
- mfidl/IMFTopology.GetTopologyID
dev_langs:
- c++
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFTopology.GetTopologyID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTopology::GetTopologyID


## -description


Gets the identifier of the topology.


## -parameters




### -param pID [out]

Receives the identifier, as a <a href="https://docs.microsoft.com/windows/desktop/medfound/topoid">TOPOID</a> value.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topoid">TOPOID</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topologies">Topologies</a>
 

 


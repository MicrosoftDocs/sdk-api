---
UID: NF:mfidl.IMFTopology.Clear
title: IMFTopology::Clear (mfidl.h)
description: Removes all nodes from the topology.
helpviewer_keywords: ["919a712f-3f1b-4681-9eeb-958ac349d8f6","Clear","Clear method [Media Foundation]","Clear method [Media Foundation]","IMFTopology interface","IMFTopology interface [Media Foundation]","Clear method","IMFTopology.Clear","IMFTopology::Clear","mf.imftopology_clear","mfidl/IMFTopology::Clear"]
old-location: mf\imftopology_clear.htm
tech.root: mf
ms.assetid: 919a712f-3f1b-4681-9eeb-958ac349d8f6
ms.date: 12/05/2018
ms.keywords: 919a712f-3f1b-4681-9eeb-958ac349d8f6, Clear, Clear method [Media Foundation], Clear method [Media Foundation],IMFTopology interface, IMFTopology interface [Media Foundation],Clear method, IMFTopology.Clear, IMFTopology::Clear, mf.imftopology_clear, mfidl/IMFTopology::Clear
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTopology::Clear
 - mfidl/IMFTopology::Clear
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTopology.Clear
---

# IMFTopology::Clear


## -description

Removes all nodes from the topology.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

You do not need to clear a topology before disposing of it. The <b>Clear</b> method is called automatically when the topology is destroyed.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>

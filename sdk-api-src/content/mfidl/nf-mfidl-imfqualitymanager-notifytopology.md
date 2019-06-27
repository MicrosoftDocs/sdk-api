---
UID: NF:mfidl.IMFQualityManager.NotifyTopology
title: IMFQualityManager::NotifyTopology (mfidl.h)
author: windows-sdk-content
description: Called when the Media Session is about to start playing a new topology.
old-location: mf\imfqualitymanager_notifytopology.htm
tech.root: medfound
ms.assetid: 5ff6d923-4a83-401a-a0de-0b1a732c31a5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 5ff6d923-4a83-401a-a0de-0b1a732c31a5, IMFQualityManager interface [Media Foundation],NotifyTopology method, IMFQualityManager.NotifyTopology, IMFQualityManager::NotifyTopology, NotifyTopology, NotifyTopology method [Media Foundation], NotifyTopology method [Media Foundation],IMFQualityManager interface, mf.imfqualitymanager_notifytopology, mfidl/IMFQualityManager::NotifyTopology
ms.topic: method
f1_keywords: 
 - "mfidl/IMFQualityManager.NotifyTopology"
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
 - IMFQualityManager.NotifyTopology
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFQualityManager::NotifyTopology


## -description



Called when the Media Session is about to start playing a new topology.




## -parameters




### -param pTopology [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the new topology. If this parameter is <b>NULL</b>, the quality manager should release any references to the previous topology.


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



In a typical quality manager this method does the following:

<ol>
<li>
Enumerates the nodes in the topology.

</li>
<li>
Calls <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject">IMFTopologyNode::GetObject</a> to get the node's underlying object.

</li>
<li>
Queries for the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a> interface.

</li>
</ol>
The quality manager can then use the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a> pointers to adjust audio-video quality as needed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager">IMFQualityManager</a>
 

 


---
UID: NF:wmcontainer.IMFASFStreamConfig.Clone
title: IMFASFStreamConfig::Clone
author: windows-sdk-content
description: Creates a copy of the Advanced Systems Format (ASF) stream configuration object.
old-location: mf\imfasfstreamconfig_clone.htm
old-project: medfound
ms.assetid: c87d658f-6569-464b-a9d0-487d44f76cc0
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: Clone, Clone method [Media Foundation], Clone method [Media Foundation],IMFASFStreamConfig interface, IMFASFStreamConfig interface [Media Foundation],Clone method, IMFASFStreamConfig.Clone, IMFASFStreamConfig::Clone, c87d658f-6569-464b-a9d0-487d44f76cc0, mf.imfasfstreamconfig_clone, wmcontainer/IMFASFStreamConfig::Clone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcontainer.h
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
tech.root: 
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamConfig.Clone
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFStreamConfig::Clone


## -description



Creates a copy of the Advanced Systems Format (ASF) stream configuration object.




## -parameters




### -param ppIStreamConfig [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a> interface of the new object. The caller must release the interface.


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



The cloned object is completely independent of the original.




## -see-also




<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>
 

 


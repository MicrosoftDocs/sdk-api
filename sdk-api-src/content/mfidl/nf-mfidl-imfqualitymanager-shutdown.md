---
UID: NF:mfidl.IMFQualityManager.Shutdown
title: IMFQualityManager::Shutdown (mfidl.h)
author: windows-sdk-content
description: Called when the Media Session is shutting down.
old-location: mf\imfqualitymanager_shutdown.htm
tech.root: medfound
ms.assetid: c71bec12-33aa-4156-a052-cf75c80df263
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFQualityManager interface [Media Foundation],Shutdown method, IMFQualityManager.Shutdown, IMFQualityManager::Shutdown, Shutdown, Shutdown method [Media Foundation], Shutdown method [Media Foundation],IMFQualityManager interface, c71bec12-33aa-4156-a052-cf75c80df263, mf.imfqualitymanager_shutdown, mfidl/IMFQualityManager::Shutdown
ms.topic: method
f1_keywords: 
 - "mfidl/IMFQualityManager.Shutdown"
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
 - IMFQualityManager.Shutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFQualityManager::Shutdown


## -description



Called when the Media Session is shutting down.




## -parameters






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



The quality manager should release all references to the Media Session when this method is called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager">IMFQualityManager</a>
 

 


---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAzAuthorizationStore::CloseApplication


## -description


The <b>CloseApplication</b> method unloads a specified <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object from the cache.

This method is not supported for XML authorization policy stores.


## -parameters




### -param bstrApplicationName [in]

The name of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object to close.


### -param lFlag [in]

Flags that control the behavior of the operation. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Child objects of the specified <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object will be unloaded from the cache only when the user closes the last handle to the <b>IAzApplication</b> object.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_AZSTORE_FORCE_APPLICATION_CLOSE"></a><a id="az_azstore_force_application_close"></a><dl>
<dt><b>AZ_AZSTORE_FORCE_APPLICATION_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
All child objects of the specified <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object will be forcefully closed. Attempts to reference an open handle to a child object of the specified <b>IAzApplication</b> object will result in an HRESULT_FROM_WIN32(ERROR_INVALID_HANDLE) error. This flag should be used only if the user has implemented code to gracefully handle the  error.

</td>
</tr>
</table>
 


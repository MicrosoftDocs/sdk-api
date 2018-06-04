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

# ISyncMgrSynchronizeCallback::LogError


## -description


Called by a registered application to log information, warning, or an error message into the error tab on the synchronization manager status dialog box.


## -parameters




### -param dwErrorLevel [in]

Type: <b>DWORD</b>

The error level. Values are taken from the <a href="https://msdn.microsoft.com/df3c3300-e203-4664-b8d5-9dc4835b33d8">SYNCMGRLOGLEVEL</a> enumeration.


### -param pszErrorText [in]

Type: <b>LPCWSTR</b>

A pointer to error text to be displayed in the error tab.


### -param pSyncLogError [in]

Type: <b>const <a href="https://msdn.microsoft.com/0220792c-90e7-4802-9ba3-3fc6ce01e4de">SYNCMGRLOGERRORINFO</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/0220792c-90e7-4802-9ba3-3fc6ce01e4de">SYNCMGRLOGERRORINFO</a> structure that contains additional error information. Registered applications that do not provide this data can pass <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and  the following:

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
The error information is logged successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/0220792c-90e7-4802-9ba3-3fc6ce01e4de">SYNCMGRLOGERRORINFO</a>



<a href="https://msdn.microsoft.com/df3c3300-e203-4664-b8d5-9dc4835b33d8">SYNCMGRLOGLEVEL</a>
 

 


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

# IWMDMLogger::LogDword


## -description



The <b>LogDword</b> method logs a <b>DWORD</b> value to the current log file. A carriage return and line feed are added to each log entry.




## -parameters




### -param dwFlags [in]

Flags that control the way a string is logged. This parameter is a combination of one or more of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMDM_LOG_SEV_INFO</td>
<td>Tag the log entry as informational.</td>
</tr>
<tr>
<td>WMDM_LOG_SEV_WARN</td>
<td>Tag the log entry as a warning.</td>
</tr>
<tr>
<td>WMDM_LOG_SEV_ERROR</td>
<td>Tag the log entry as an error.</td>
</tr>
<tr>
<td>WMDM_LOG_NOTIMESTAMP</td>
<td>Do not include a time stamp on the log entry. Time stamps are in ISO format minus the time-zone information.</td>
</tr>
</table>
 


### -param pszSrcName [in]

Optional pointer to a string containing the name of the module that is making the log entry.


### -param pszLogFormat [in]

Pointer to a string that specifies the format of the log string. This string is of the same form as the format string for the <b>printf</b> function.


### -param dwLog [in]

<b>DWORD</b> value to log.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad">Enabling Logging</a>



<a href="https://msdn.microsoft.com/bededb91-f343-455b-a3ef-548e6f961933">IWMDMLogger Interface</a>
 

 


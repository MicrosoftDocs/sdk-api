---
UID: NF:shellscalingapi.GetProcessDpiAwareness
title: GetProcessDpiAwareness function
author: windows-sdk-content
description: Retrieves the dots per inch (dpi) awareness of the specified process.
old-location: hidpi\getprocessdpiawareness.htm
old-project: hidpi
ms.assetid: FC99DBC7-D710-49EF-B114-6CE6F1AE2454
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetProcessDpiAwareness, GetProcessDpiAwareness function [High DPI], hidpi.getprocessdpiawareness, shellscalingapi/GetProcessDpiAwareness, winmsg.GetProcessDpiAwareness
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellscalingapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: SHELL_UI_COMPONENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - shcore.dll
 - api-ms-win-shcore-scaling-l1-1-1.dll
 - API-MS-Win-ShCore-Scaling-L1-1-2.dll
api_name:
 - GetProcessDpiAwareness
product: Windows
targetos: Windows
req.lib: Shcore.lib
req.dll: Shcore.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# GetProcessDpiAwareness function


## -description


Retrieves the dots per inch (dpi) awareness of the specified process.


## -parameters




### -param hprocess [in]

Handle of the process that is being queried. If this parameter is NULL, the current process is queried.


### -param value [out]

The DPI awareness of the specified process. Possible values are from the <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a> enumeration.


## -returns



This function returns one of the following values.

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
The function successfully retrieved the DPI awareness of the specified process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle or pointer passed in is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The application does not have sufficient privileges.

</td>
</tr>
</table>
 




## -remarks



This function is identical to the following code: 

<code>GetAwarenessFromDpiAwarenessContext(GetThreadDpiAwarenessContext());</code>




## -see-also




<a href="https://msdn.microsoft.com/BE4DC6B9-BCD6-4E27-81F8-E3CF054CFBE9">GetAwarenessFromDpiAwarenessContext</a>



<a href="https://msdn.microsoft.com/DE86D551-974F-4A03-BDBE-348592CAB81F">GetThreadDpiAwarenessContext</a>



<a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a>
 

 


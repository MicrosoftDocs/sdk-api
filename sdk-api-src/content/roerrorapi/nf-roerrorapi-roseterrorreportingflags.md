---
UID: NF:roerrorapi.RoSetErrorReportingFlags
title: RoSetErrorReportingFlags function
author: windows-sdk-content
description: Sets the reporting behavior of Windows Runtime error functions.
old-location: winrt\roseterrorreportingflags.htm
old-project: WinRT
ms.assetid: 167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: RoSetErrorReportingFlags, RoSetErrorReportingFlags function [Windows Runtime], WinRTSetErrorReportingFlags, roerrorapi/RoSetErrorReportingFlags, roerrorapi/WinRTSetErrorReportingFlags, winrt.roseterrorreportingflags, winrt.winrtseterrorreportingflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: roerrorapi.h
req.include-header: Roapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - roerrorapi.h
 - API-MS-Win-Core-WinRT-error-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - RoSetErrorReportingFlags
 - WinRTSetErrorReportingFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RoSetErrorReportingFlags function


## -description


Sets the reporting behavior of Windows Runtime error functions.


## -parameters




### -param flags [in]

Type: <b>UINT32</b>

A bitmask of <a href="https://msdn.microsoft.com/345E1C4D-4A2F-4E18-9E70-4B8AE25FE8FD">RO_ERROR_REPORTING_FLAGS</a> values.


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

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
The  error-reporting behavior was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>flags</i> has invalid or undefined bits set.

</td>
</tr>
</table>
 




## -remarks



Get the current reporting behavior of   Windows Runtime error functions by calling the <a href="https://msdn.microsoft.com/0DCF6693-5066-46E3-A7F9-5CF0780FA87C">RoGetErrorReportingFlags</a> function.




## -see-also




<a href="https://msdn.microsoft.com/345E1C4D-4A2F-4E18-9E70-4B8AE25FE8FD">RO_ERROR_REPORTING_FLAGS</a>



<a href="https://msdn.microsoft.com/0DCF6693-5066-46E3-A7F9-5CF0780FA87C">RoGetErrorReportingFlags</a>



<a href="https://msdn.microsoft.com/ED647880-5A18-4F75-B7E5-3B9BF36229D3">RoOriginateError</a>



<a href="https://msdn.microsoft.com/167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE">RoSetErrorReportingFlags</a>



<a href="https://msdn.microsoft.com/B0921292-1EEA-4154-8AB4-B654A9B31DA6">RoTransformError</a>
 

 


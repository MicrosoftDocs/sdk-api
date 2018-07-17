---
UID: NF:roerrorapi.RoGetErrorReportingFlags
title: RoGetErrorReportingFlags function
author: windows-sdk-content
description: Gets the current reporting behavior of Windows Runtime error functions.
old-location: winrt\rogeterrorreportingflags.htm
old-project: WinRT
ms.assetid: 0DCF6693-5066-46E3-A7F9-5CF0780FA87C
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: RoGetErrorReportingFlags, RoGetErrorReportingFlags function [Windows Runtime], WinRTGetErrorReportingFlags, roerrorapi/RoGetErrorReportingFlags, roerrorapi/WinRTGetErrorReportingFlags, winrt.rogeterrorreportingflags, winrt.winrtgeterrorreportingflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: roerrorapi.h
req.include-header: 
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
 - RoGetErrorReportingFlags
 - WinRTGetErrorReportingFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# RoGetErrorReportingFlags function


## -description


Gets the current reporting behavior of Windows Runtime error functions.


## -parameters




### -param pflags [out]

Type: <b>UINT32*</b>

A pointer to the bitmask of <a href="https://msdn.microsoft.com/345E1C4D-4A2F-4E18-9E70-4B8AE25FE8FD">RO_ERROR_REPORTING_FLAGS</a> values that represents the current error-reporting behavior.


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
The  error-reporting behavior was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pflags</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Set the reporting behavior of   Windows Runtime error functions by calling the  <a href="https://msdn.microsoft.com/167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE">RoSetErrorReportingFlags</a>  function.




## -see-also




<a href="https://msdn.microsoft.com/345E1C4D-4A2F-4E18-9E70-4B8AE25FE8FD">RO_ERROR_REPORTING_FLAGS</a>



<a href="https://msdn.microsoft.com/ED647880-5A18-4F75-B7E5-3B9BF36229D3">RoOriginateError</a>



<a href="https://msdn.microsoft.com/167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE">RoSetErrorReportingFlags</a>



<a href="https://msdn.microsoft.com/B0921292-1EEA-4154-8AB4-B654A9B31DA6">RoTransformError</a>
 

 


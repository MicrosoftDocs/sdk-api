---
UID: NF:roerrorapi.RoGetErrorReportingFlags
title: RoGetErrorReportingFlags function
description: Gets the current reporting behavior of Windows Runtime error functions.
helpviewer_keywords: ["RoGetErrorReportingFlags","RoGetErrorReportingFlags function [Windows Runtime]","WinRTGetErrorReportingFlags","roerrorapi/RoGetErrorReportingFlags","roerrorapi/WinRTGetErrorReportingFlags","winrt.rogeterrorreportingflags","winrt.winrtgeterrorreportingflags"]
old-location: winrt\rogeterrorreportingflags.htm
tech.root: WinRT
ms.assetid: 0DCF6693-5066-46E3-A7F9-5CF0780FA87C
ms.date: 12/5/2018
ms.keywords: RoGetErrorReportingFlags, RoGetErrorReportingFlags function [Windows Runtime], WinRTGetErrorReportingFlags, roerrorapi/RoGetErrorReportingFlags, roerrorapi/WinRTGetErrorReportingFlags, winrt.rogeterrorreportingflags, winrt.winrtgeterrorreportingflags
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - RoGetErrorReportingFlags
 - roerrorapi/RoGetErrorReportingFlags
dev_langs:
 - c++
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
---

# RoGetErrorReportingFlags function


## -description

Gets the current reporting behavior of Windows Runtime error functions.

## -parameters

### -param pflags [out]

Type: <b>UINT32*</b>

A pointer to the bitmask of <a href="/windows/desktop/api/roerrorapi/ne-roerrorapi-roerrorreportingflags">RO_ERROR_REPORTING_FLAGS</a> values that represents the current error-reporting behavior.

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

Set the reporting behavior of   Windows Runtime error functions by calling the  <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags">RoSetErrorReportingFlags</a>  function.

## -see-also

<a href="/windows/desktop/api/roerrorapi/ne-roerrorapi-roerrorreportingflags">RO_ERROR_REPORTING_FLAGS</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">RoOriginateError</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags">RoSetErrorReportingFlags</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerror">RoTransformError</a>
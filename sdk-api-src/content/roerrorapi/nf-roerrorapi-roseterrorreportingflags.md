---
UID: NF:roerrorapi.RoSetErrorReportingFlags
title: RoSetErrorReportingFlags function
description: Sets the reporting behavior of Windows Runtime error functions.
helpviewer_keywords: ["RoSetErrorReportingFlags","RoSetErrorReportingFlags function [Windows Runtime]","WinRTSetErrorReportingFlags","roerrorapi/RoSetErrorReportingFlags","roerrorapi/WinRTSetErrorReportingFlags","winrt.roseterrorreportingflags","winrt.winrtseterrorreportingflags"]
old-location: winrt\roseterrorreportingflags.htm
tech.root: WinRT
ms.assetid: 167C2EC9-9EA0-4E1D-840B-DAF5F47ED1FE
ms.date: 12/5/2018
ms.keywords: RoSetErrorReportingFlags, RoSetErrorReportingFlags function [Windows Runtime], WinRTSetErrorReportingFlags, roerrorapi/RoSetErrorReportingFlags, roerrorapi/WinRTSetErrorReportingFlags, winrt.roseterrorreportingflags, winrt.winrtseterrorreportingflags
req.header: roerrorapi.h
req.include-header: Roapi.h
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
 - RoSetErrorReportingFlags
 - roerrorapi/RoSetErrorReportingFlags
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
 - RoSetErrorReportingFlags
 - WinRTSetErrorReportingFlags
---

# RoSetErrorReportingFlags function


## -description

Sets the reporting behavior of Windows Runtime error functions.

## -parameters

### -param flags [in]

Type: <b>UINT32</b>

A bitmask of <a href="/windows/desktop/api/roerrorapi/ne-roerrorapi-roerrorreportingflags">RO_ERROR_REPORTING_FLAGS</a> values.

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

Get the current reporting behavior of   Windows Runtime error functions by calling the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags">RoGetErrorReportingFlags</a> function.

## -see-also

<a href="/windows/desktop/api/roerrorapi/ne-roerrorapi-roerrorreportingflags">RO_ERROR_REPORTING_FLAGS</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags">RoGetErrorReportingFlags</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">RoOriginateError</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags">RoSetErrorReportingFlags</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerror">RoTransformError</a>
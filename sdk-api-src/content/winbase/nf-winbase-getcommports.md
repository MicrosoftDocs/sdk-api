---
UID: NF:winbase.GetCommPorts
title: GetCommPorts function (winbase.h)
description: Gets an array that contains the well-formed COM ports.
helpviewer_keywords: ["GetCommPorts","GetCommPorts function","base.getcommports","winbase/GetCommPorts"]
old-location: base\getcommports.htm
tech.root: base
ms.assetid: 8E57FB62-D7A0-4B47-942B-E33E0B7A37B1
ms.date: 12/05/2018
ms.keywords: GetCommPorts, GetCommPorts function, base.getcommports, winbase/GetCommPorts
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OneCore.lib
req.dll: KernelBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCommPorts
 - winbase/GetCommPorts
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-comm-l1-1-2.dll
 - KernelBase.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCommPorts
---

# GetCommPorts function


## -description

Gets an array that contains the well-formed COM ports.

This function obtains the COM port numbers from the <b>HKLM\Hardware\DeviceMap\SERIALCOMM</b> registry key and then writes them to a caller-supplied array. If the array is too small, the function gets the necessary size. 
<div class="alert"><b>Note</b>  If new entries are added to the registry key, the necessary size can change between API calls.</div><div> </div>

## -parameters

### -param lpPortNumbers [out]

An array for the port numbers.

### -param uPortNumbersCount [in]

The length of the array in the <i>lpPortNumbers</i> parameter.

### -param puPortNumbersFound [out]

The number of port numbers written to the <i>lpPortNumbers</i> or the length of the array required for the port numbers.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded. The <i>lpPortNumbers</i> array was large enough for the result.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpPortNumbers</i> array was too small to contain all available port numbers. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
There are no comm ports available.

</td>
</tr>
</table>


---
UID: NF:shlobj_core.IsNetDrive
title: IsNetDrive function
author: windows-sdk-content
description: Tests whether a drive is a network drive.
old-location: shell\IsNetDrive.htm
tech.root: Shell
ms.assetid: 44e02665-648a-4cf0-9dc0-038e54d08a49
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IsNetDrive, IsNetDrive function [Windows Shell], _win32_IsNetDrive, shell.IsNetDrive, shlobj_core/IsNetDrive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - IsNetDrive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsNetDrive function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows. Use <a href="https://msdn.microsoft.com/b3989a3f-fc90-4ea0-8d3e-8e57068a08bc">GetDriveType</a> or <a href="https://msdn.microsoft.com/72d84752-4e64-4c16-872b-cb892dffbf9a">WNetGetConnection</a> instead.]

Tests whether a drive is a network drive.


## -parameters




### -param iDrive [in]

Type: <b>int</b>

An integer that indicates which drive letter you want to test. Set it to 0 for  A:, 1 for B:, and so on.


## -returns



Type: <b>int</b>

This function returns one of the following values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The specified drive is not a network drive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The specified drive is a network drive that is properly connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The specified drive is a network drive that is disconnected or in an error state.

</td>
</tr>
</table>
 




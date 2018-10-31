---
UID: NF:shlwapi.MAKEDLLVERULL
title: MAKEDLLVERULL macro
author: windows-sdk-content
description: Used to pack DLL version information into a ULONGLONG value.
old-location: shell\MAKEDLLVERULL.htm
tech.root: shell
ms.assetid: 10c75c91-9642-4877-845e-8c6343721b4f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MAKEDLLVERULL, MAKEDLLVERULL macro [Windows Shell], _win32_MAKEDLLVERULL, shell.MAKEDLLVERULL, shlwapi/MAKEDLLVERULL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - MAKEDLLVERULL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MAKEDLLVERULL macro


## -description


Used to pack DLL version information into a ULONGLONG value.


## -parameters




### -param major

The major version number.


### -param minor

The minor version number.


### -param build

The build number.


### -param qfe

The hotfix number that identifies the service pack.


## -remarks



This macro is used in conjunction with <a href="https://msdn.microsoft.com/d7ec0f7d-ba2f-4aa4-b867-a2615244a580">DllGetVersion</a> to pack version information into a form that can easily be compared to the <b>ullVersion</b> member of a <a href="https://msdn.microsoft.com/1648924d-0727-4cee-80d3-f97550f235cd">DLLVERSIONINFO2</a> structure. It is defined as follows.

				

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define MAKEDLLVERULL(major, minor, build, sp) \
        (((ULONGLONG)(major) &lt;&lt; 48) | \
         ((ULONGLONG)(minor) &lt;&lt; 32) | \
         ((ULONGLONG)(build) &lt;&lt; 16) | \
         ((ULONGLONG)(   sp) &lt;&lt;  0))
</pre>
</td>
</tr>
</table></span></div>
For most purposes, you only need to assign values to the major and minor version numbers. The remaining two parameters can be set to zero. The following code fragment illustrates how to use <b>MAKEDLLVERULL</b> to determine whether a DLL is <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">version 4.71</a> or later. The <b>VersionInfo</b> structure is the <a href="https://msdn.microsoft.com/1648924d-0727-4cee-80d3-f97550f235cd">DLLVERSIONINFO2</a> structure returned by <a href="https://msdn.microsoft.com/d7ec0f7d-ba2f-4aa4-b867-a2615244a580">DllGetVersion</a>.

				

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if(VersionInfo.ullVersion &gt;= MAKEDLLVERULL(4, 71, 0, 0))
{
    ...
}
</pre>
</td>
</tr>
</table></span></div>



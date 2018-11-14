---
UID: NF:msi.MsiQueryProductStateW
title: MsiQueryProductStateW function
author: windows-sdk-content
description: The MsiQueryProductState function returns the installed state for a product.
old-location: setup\msiqueryproductstate.htm
tech.root: msi
ms.assetid: f26f3229-d1ce-4802-99b1-857c6501c828
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MsiQueryProductState, MsiQueryProductState function, MsiQueryProductStateA, MsiQueryProductStateW, _msi_msiqueryproductstate, msi/MsiQueryProductState, msi/MsiQueryProductStateA, msi/MsiQueryProductStateW, setup.msiqueryproductstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiQueryProductStateW (Unicode) and MsiQueryProductStateA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiQueryProductState
 - MsiQueryProductStateA
 - MsiQueryProductStateW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MsiQueryProductStateW
: 
---

# MsiQueryProductStateW function


## -description


The 
<b>MsiQueryProductState</b> function returns the installed state for a product.


## -parameters




### -param szProduct [in]

Specifies the product code that identifies the product to be queried.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The product is installed for a different user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
The product is advertised but not installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The product is installed for the current user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The product is neither advertised or installed.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">System Status Functions</a>
 

 


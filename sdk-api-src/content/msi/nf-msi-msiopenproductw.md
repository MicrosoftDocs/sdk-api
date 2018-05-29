---
UID: NF:msi.MsiOpenProductW
title: MsiOpenProductW function
author: windows-sdk-content
description: The MsiOpenProduct function opens a product for use with the functions that access the product database. The MsiCloseHandle function must be called with the handle when the handle is no longer needed.
old-location: setup\msiopenproduct.htm
old-project: Msi
ms.assetid: fdc5a2f5-c44a-4cb3-b206-a598bd60024b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: MsiOpenProduct, MsiOpenProduct function, MsiOpenProductA, MsiOpenProductW, _msi_msiopenproduct, msi/MsiOpenProduct, msi/MsiOpenProductA, msi/MsiOpenProductW, setup.msiopenproduct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiOpenProductW (Unicode) and MsiOpenProductA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRM_LICENSE_ACQ_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiOpenProduct
-	MsiOpenProductA
-	MsiOpenProductW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiOpenProductW function


## -description


The 
<b>MsiOpenProduct</b> function opens a product for use with the functions that access the product database. The 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a> function must be called with the handle when the handle is no longer needed.
<div class="alert"><b>Note</b>  Initialize COM on the same thread before calling the <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <b>MsiOpenProduct</b> function.
</div><div> </div>

## -parameters




### -param szProduct [in]

Specifies the product code of the product to be opened.


### -param hProduct [out]

Pointer to a variable that receives the product handle.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration information is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The product could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SOURCE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The source was unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product code was unrecognized.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Product Query Functions</a>
 

 


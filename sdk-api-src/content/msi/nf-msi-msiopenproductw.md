---
UID: NF:msi.MsiOpenProductW
title: MsiOpenProductW function (msi.h)
author: windows-sdk-content
description: The MsiOpenProduct function opens a product for use with the functions that access the product database. The MsiCloseHandle function must be called with the handle when the handle is no longer needed.
old-location: setup\msiopenproduct.htm
tech.root: Msi
ms.assetid: fdc5a2f5-c44a-4cb3-b206-a598bd60024b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MsiOpenProduct, MsiOpenProduct function, MsiOpenProductA, MsiOpenProductW, _msi_msiopenproduct, msi/MsiOpenProduct, msi/MsiOpenProductA, msi/MsiOpenProductW, setup.msiopenproduct
ms.topic: function
f1_keywords: ["msi/MsiOpenProduct"]
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
 - MsiOpenProduct
 - MsiOpenProductA
 - MsiOpenProductW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiOpenProductW function


## -description


The 
<b>MsiOpenProduct</b> function opens a product for use with the functions that access the product database. The 
<a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a> function must be called with the handle when the handle is no longer needed.
<div class="alert"><b>Note</b>  Initialize COM on the same thread before calling the <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <b>MsiOpenProduct</b> function.
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




<a href="https://docs.microsoft.com/windows/desktop/Msi/installer-function-reference">Product Query Functions</a>
 

 


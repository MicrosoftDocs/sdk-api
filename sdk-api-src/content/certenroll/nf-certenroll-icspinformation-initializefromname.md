---
UID: NF:certenroll.ICspInformation.InitializeFromName
title: ICspInformation::InitializeFromName
author: windows-sdk-content
description: Initializes the object from a string that contains a provider name.
old-location: security\icspinformation_initializefromname_method.htm
tech.root: SecCertEnroll
ms.assetid: b405503f-2af5-4a2f-abdb-e2eb108c4b1b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICspInformation interface [Security],InitializeFromName method, ICspInformation.InitializeFromName, ICspInformation::InitializeFromName, InitializeFromName, InitializeFromName method [Security], InitializeFromName method [Security],ICspInformation interface, certenroll/ICspInformation::InitializeFromName, security.icspinformation_initializefromname_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspInformation.InitializeFromName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- ICspInformation.InitializeFromName
: 
---

# ICspInformation::InitializeFromName


## -description


The <b>InitializeFromName</b> method initializes the object from a string that contains a provider name. This method is web enabled.


## -parameters




### -param strName [in]

A <b>BSTR</b> variable that contains the name.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>InitializeFromName</b> method opens the named provider and queries it to set the following property values on the <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> object:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376605(v=VS.85).aspx">CspAlgorithms</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376743(v=VS.85).aspx">HasHardwareRandomNumberGenerator</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376747(v=VS.85).aspx">IsHardwareDevice</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376748(v=VS.85).aspx">IsRemovable</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb394685(v=VS.85).aspx">IsSmartCard</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376750(v=VS.85).aspx">IsSoftwareDevice</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376751(v=VS.85).aspx">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376752(v=VS.85).aspx">LegacyCsp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376753(v=VS.85).aspx">MaxKeyContainerNameLength</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376755(v=VS.85).aspx">Name</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376757(v=VS.85).aspx">Type</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376758(v=VS.85).aspx">Valid</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376759(v=VS.85).aspx">Version</a>
</li>
</ul>


The method adds the available algorithms to the <a href="https://msdn.microsoft.com/en-us/library/Aa375948(v=VS.85).aspx">ICspAlgorithms</a> collection returned by the <a href="https://msdn.microsoft.com/en-us/library/Aa376605(v=VS.85).aspx">CspAlgorithms</a> property. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa376746(v=VS.85).aspx">InitializeFromType</a> method to initialize the object from a provider type.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>
 

 


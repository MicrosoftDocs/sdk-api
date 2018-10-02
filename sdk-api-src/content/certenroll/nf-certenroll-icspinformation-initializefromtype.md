---
UID: NF:certenroll.ICspInformation.InitializeFromType
title: ICspInformation::InitializeFromType
author: windows-sdk-content
description: Initializes the object from the default cryptographic provider.
old-location: security\icspinformation_initializefromtype_method.htm
tech.root: SecCertEnroll
ms.assetid: 24466981-2ea2-41f5-b2db-85b5629fba7d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICspInformation interface [Security],InitializeFromType method, ICspInformation.InitializeFromType, ICspInformation::InitializeFromType, InitializeFromType, InitializeFromType method [Security], InitializeFromType method [Security],ICspInformation interface, certenroll/ICspInformation::InitializeFromType, security.icspinformation_initializefromtype_method
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
 - ICspInformation.InitializeFromType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspInformation::InitializeFromType


## -description


The <b>InitializeFromType</b> method initializes the object from the default cryptographic provider.


## -parameters




### -param Type [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa379427(v=VS.85).aspx">X509ProviderType</a> enumeration value that defines the provider type.

<ul>
<li>If you specify XCN_PROV_NONE and set the <i>pAlgorithm</i> parameter to a value other than <b>NULL</b>, the default  Cryptography API: Next Generation (CNG) provider is used.</li>
<li>If you specify a value other than XCN_PROV_NONE and set the <i>pAlgorithm</i> parameter to <b>NULL</b>, the default legacy cryptographic service provider (CSP) is used.</li>
</ul>

### -param pAlgorithm [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface that represents an algorithm OID. This parameter is optional and can be <b>NULL</b>. For more information, see the <i>Type</i> parameter.


### -param MachineContext [in]

A <b>VARIANT_BOOL</b> variable that indicates whether to use the computer or user context to determine the default provider for the specified provider type. Specify <b>VARIANT_TRUE</b> for the computer and <b>VARIANT_FALSE</b> for the user.


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



The <b>InitializeFromType</b> method validates the specified type and saves it in the <a href="https://msdn.microsoft.com/en-us/library/Aa376757(v=VS.85).aspx">Type</a> property, retrieves the default provider, and sets the following property values on the <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> object:<ul>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa376758(v=VS.85).aspx">Valid</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa376759(v=VS.85).aspx">Version</a>
</li>
</ul>


The method adds the available algorithms to the <a href="https://msdn.microsoft.com/en-us/library/Aa375948(v=VS.85).aspx">ICspAlgorithms</a> collection returned by the <a href="https://msdn.microsoft.com/en-us/library/Aa376605(v=VS.85).aspx">CspAlgorithms</a> property. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa376745(v=VS.85).aspx">InitializeFromName</a> method to initialize the object from a CSP name.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>
 

 


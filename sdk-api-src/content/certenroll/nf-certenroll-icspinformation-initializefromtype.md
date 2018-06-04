---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICspInformation::InitializeFromType


## -description


The <b>InitializeFromType</b> method initializes the object from the default cryptographic provider.


## -parameters




### -param Type [in]

An <a href="https://msdn.microsoft.com/636ccb3a-ea66-4993-ac62-29409ce63eba">X509ProviderType</a> enumeration value that defines the provider type.

<ul>
<li>If you specify XCN_PROV_NONE and set the <i>pAlgorithm</i> parameter to a value other than <b>NULL</b>, the default  Cryptography API: Next Generation (CNG) provider is used.</li>
<li>If you specify a value other than XCN_PROV_NONE and set the <i>pAlgorithm</i> parameter to <b>NULL</b>, the default legacy cryptographic service provider (CSP) is used.</li>
</ul>

### -param pAlgorithm [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface that represents an algorithm OID. This parameter is optional and can be <b>NULL</b>. For more information, see the <i>Type</i> parameter.


### -param MachineContext [in]

A <b>VARIANT_BOOL</b> variable that indicates whether to use the computer or user context to determine the default provider for the specified provider type. Specify <b>VARIANT_TRUE</b> for the computer and <b>VARIANT_FALSE</b> for the user.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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



The <b>InitializeFromType</b> method validates the specified type and saves it in the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property, retrieves the default provider, and sets the following property values on the <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object:<ul>
<li>
<a href="https://msdn.microsoft.com/e74f1aa3-883b-40e4-8052-6651eaa4b63f">CspAlgorithms</a>
</li>
<li>
<a href="https://msdn.microsoft.com/49d79310-90d2-4874-beaf-284abefd950f">HasHardwareRandomNumberGenerator</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d69ade8c-3b74-4391-9048-6511f3d7e9fa">IsHardwareDevice</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ee67670b-80a9-4637-a5ed-84d3430853ea">IsRemovable</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cfb88e17-39bb-4b4f-9eb3-3691376f8285">IsSmartCard</a>
</li>
<li>
<a href="https://msdn.microsoft.com/50f78dcc-4d32-40c9-8153-f0b6ac72c03b">IsSoftwareDevice</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f66f2f5c-7f50-4be6-973e-844d6cb76f61">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f798401c-bc78-438d-8847-82a57589ce38">LegacyCsp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2508786f-0892-4ece-bbef-bd8ed9c81eee">MaxKeyContainerNameLength</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>
</li>
<li>
<a href="https://msdn.microsoft.com/507896b0-598c-4a2d-854e-d4d266fdfaf7">Valid</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn973197">Version</a>
</li>
</ul>


The method adds the available algorithms to the <a href="https://msdn.microsoft.com/bbf8cff4-b1b2-480e-8c30-eb34166db143">ICspAlgorithms</a> collection returned by the <a href="https://msdn.microsoft.com/e74f1aa3-883b-40e4-8052-6651eaa4b63f">CspAlgorithms</a> property. Call the <a href="https://msdn.microsoft.com/b405503f-2af5-4a2f-abdb-e2eb108c4b1b">InitializeFromName</a> method to initialize the object from a CSP name.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
 

 


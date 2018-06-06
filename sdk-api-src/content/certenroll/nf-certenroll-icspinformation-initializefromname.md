---
UID: NF:certenroll.ICspInformation.InitializeFromName
title: ICspInformation::InitializeFromName
author: windows-sdk-content
description: Initializes the object from a string that contains a provider name.
old-location: security\icspinformation_initializefromname_method.htm
old-project: SecCertEnroll
ms.assetid: b405503f-2af5-4a2f-abdb-e2eb108c4b1b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ICspInformation interface [Security],InitializeFromName method, ICspInformation.InitializeFromName, ICspInformation::InitializeFromName, InitializeFromName, InitializeFromName method [Security], InitializeFromName method [Security],ICspInformation interface, certenroll/ICspInformation::InitializeFromName, security.icspinformation_initializefromname_method
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformation::InitializeFromName


## -description


The <b>InitializeFromName</b> method initializes the object from a string that contains a provider name. This method is web enabled.


## -parameters




### -param strName [in]

A <b>BSTR</b> variable that contains the name.


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



The <b>InitializeFromName</b> method opens the named provider and queries it to set the following property values on the <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object:<ul>
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>
</li>
<li>
<a href="https://msdn.microsoft.com/507896b0-598c-4a2d-854e-d4d266fdfaf7">Valid</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn973197">Version</a>
</li>
</ul>


The method adds the available algorithms to the <a href="https://msdn.microsoft.com/bbf8cff4-b1b2-480e-8c30-eb34166db143">ICspAlgorithms</a> collection returned by the <a href="https://msdn.microsoft.com/e74f1aa3-883b-40e4-8052-6651eaa4b63f">CspAlgorithms</a> property. Call the <a href="https://msdn.microsoft.com/24466981-2ea2-41f5-b2db-85b5629fba7d">InitializeFromType</a> method to initialize the object from a provider type.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
 

 


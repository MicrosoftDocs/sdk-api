---
UID: NF:certenroll.ICertPropertyKeyProvInfo.Initialize
title: ICertPropertyKeyProvInfo::Initialize
author: windows-sdk-content
description: Initializes the object from a private key.
old-location: security\icertpropertykeyprovinfo_initialize_method.htm
tech.root: SecCertEnroll
ms.assetid: bc317b7b-c4d8-480b-9de7-3324e30898b8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICertPropertyKeyProvInfo interface [Security],Initialize method, ICertPropertyKeyProvInfo.Initialize, ICertPropertyKeyProvInfo::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertPropertyKeyProvInfo interface, certenroll/ICertPropertyKeyProvInfo::Initialize, security.icertpropertykeyprovinfo_initialize_method
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
 - ICertPropertyKeyProvInfo.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyKeyProvInfo::Initialize


## -description


The <b>Initialize</b> method initializes the object from a private key.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> interface that represents the private key.


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
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> pointer is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_ARITHMETIC_OVERFLOW</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The unique container name and the provider name are too long.

</td>
</tr>
</table>
 




## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375928(v=VS.85).aspx">SetValueOnCertificate</a> method to associate the property with a certificate. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa375744(v=VS.85).aspx">PrivateKey</a> property to retrieve the key.

The <b>Initialize</b> method opens the private key and verifies that the following <a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a> properties are set:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378966(v=VS.85).aspx">CspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378953(v=VS.85).aspx">ContainerName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379037(v=VS.85).aspx">UniqueContainerName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379032(v=VS.85).aspx">ProviderType</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379024(v=VS.85).aspx">MachineContext</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375725(v=VS.85).aspx">ICertPropertyKeyProvInfo</a>
 

 


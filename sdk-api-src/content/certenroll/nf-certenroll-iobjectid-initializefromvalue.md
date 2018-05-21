---
UID: NF:certenroll.IObjectId.InitializeFromValue
title: IObjectId::InitializeFromValue
author: windows-driver-content
description: Initializes the object from a string that contains a dotted decimal object identifier (OID).
old-location: security\iobjectid_initializefromvalue_method.htm
old-project: SecCertEnroll
ms.assetid: 2bb2ee69-02c3-41b9-a67b-036c7154a44e
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IObjectId interface [Security],InitializeFromValue method, IObjectId.InitializeFromValue, IObjectId::InitializeFromValue, InitializeFromValue, InitializeFromValue method [Security], InitializeFromValue method [Security],IObjectId interface, certenroll/IObjectId::InitializeFromValue, security.iobjectid_initializefromvalue_method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IObjectId.InitializeFromValue
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IObjectId::InitializeFromValue


## -description


The <b>InitializeFromValue</b> method initializes the object from a string that contains a dotted decimal <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID). This method is web enabled. 


## -parameters




### -param strValue [in]

A <b>BSTR</b> variable that contains the dotted decimal representation of the ASN.1 object identifier. For example, the value 1.2.840.10045.4.1. represents the iso(1)member-body(2)us(840)10045 signatures(4)sha1(1) object identifier.


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
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The OID information could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CRYPT_E_UNKNOWN_ALGO</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The algorithm name is not recognized.

</td>
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



You can call the following properties to retrieve information about an initialized <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> object:<ul>
<li>
<a href="https://msdn.microsoft.com/9360f652-afeb-4f30-a423-402f397b9255">FriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn923306">Value</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectID</a>
 

 


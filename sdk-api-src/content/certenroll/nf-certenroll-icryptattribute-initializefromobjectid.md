---
UID: NF:certenroll.ICryptAttribute.InitializeFromObjectId
title: ICryptAttribute::InitializeFromObjectId
author: windows-sdk-content
description: Initializes a cryptographic attribute by using an object identifier.
old-location: security\icryptattribute_initializefromobjectid_method.htm
tech.root: SecCertEnroll
ms.assetid: 6825cca7-c3a5-46a8-9be5-851344629929
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICryptAttribute interface [Security],InitializeFromObjectId method, ICryptAttribute.InitializeFromObjectId, ICryptAttribute::InitializeFromObjectId, InitializeFromObjectId, InitializeFromObjectId method [Security], InitializeFromObjectId method [Security],ICryptAttribute interface, certenroll/ICryptAttribute::InitializeFromObjectId, security.icryptattribute_initializefromobjectid_method
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
 - ICryptAttribute.InitializeFromObjectId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICryptAttribute::InitializeFromObjectId


## -description


The <b>InitializeFromObjectId</b> method initializes a cryptographic attribute by using an object identifier.


## -parameters




### -param pObjectId [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface that contains the object identifier of the attribute.


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
The pointer to the <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



You must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> object by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa376797(v=VS.85).aspx">InitializeFromName</a> or <a href="https://msdn.microsoft.com/en-us/library/Aa376798(v=VS.85).aspx">InitializeFromValue</a> methods before using it in this method. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 


---
UID: NF:certenroll.IX509Attribute.Initialize
title: IX509Attribute::Initialize
author: windows-sdk-content
description: Initializes the object from an object identifier (OID) and a value.
old-location: security\ix509attribute_initialize_method.htm
old-project: seccertenroll
ms.assetid: 82457ca3-4aae-4f47-950c-1146c8614a5b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509Attribute interface [Security],Initialize method, IX509Attribute.Initialize, IX509Attribute::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509Attribute interface, certenroll/IX509Attribute::Initialize, security.ix509attribute_initialize_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - IX509Attribute.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509Attribute::Initialize


## -description


The <b>Initialize</b> method initializes the object from  an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) and a value.


## -parameters




### -param pObjectId [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface that contains the attribute OID.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the attribute value contained in the <i>strEncodedData</i> parameter.


### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the attribute value.


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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
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

Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377120(v=VS.85).aspx">ObjectId</a> property to retrieve the OID. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377122(v=VS.85).aspx">RawData</a> property to retrieve the attribute value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 


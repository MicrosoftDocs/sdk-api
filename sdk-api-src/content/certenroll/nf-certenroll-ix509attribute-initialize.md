---
UID: NF:certenroll.IX509Attribute.Initialize
title: IX509Attribute::Initialize
author: windows-sdk-content
description: Initializes the object from an object identifier (OID) and a value.
old-location: security\ix509attribute_initialize_method.htm
tech.root: SecCertEnroll
ms.assetid: 82457ca3-4aae-4f47-950c-1146c8614a5b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509Attribute interface [Security],Initialize method, IX509Attribute.Initialize, IX509Attribute::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509Attribute interface, certenroll/IX509Attribute::Initialize, security.ix509attribute_initialize_method
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
 - IX509Attribute.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Attribute::Initialize


## -description


The <b>Initialize</b> method initializes the object from  an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and a value.


## -parameters




### -param pObjectId [in]

Pointer to an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface that contains the attribute OID.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the attribute value contained in the <i>strEncodedData</i> parameter.


### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the attribute value.


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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The pointer to the <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



You must initialize the <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> object by calling the <a href="https://msdn.microsoft.com/dce84308-aecc-4841-88da-e948313b90b3">InitializeFromName</a> or <a href="https://msdn.microsoft.com/2bb2ee69-02c3-41b9-a67b-036c7154a44e">InitializeFromValue</a> methods before using it in this method.

Call the <a href="https://msdn.microsoft.com/a65c7989-5e6e-4253-8ddc-1d1207fecaf8">ObjectId</a> property to retrieve the OID. Call the <a href="https://msdn.microsoft.com/a8e67f3c-4c05-4742-8251-a03335054b2e">RawData</a> property to retrieve the attribute value.




## -see-also




<a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 


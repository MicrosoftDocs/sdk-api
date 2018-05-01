---
UID: NF:certenroll.ICryptAttribute.InitializeFromObjectId
title: ICryptAttribute::InitializeFromObjectId method
author: windows-driver-content
description: Initializes a cryptographic attribute by using an object identifier.
old-location: security\icryptattribute_initializefromobjectid_method.htm
old-project: SecCertEnroll
ms.assetid: 6825cca7-c3a5-46a8-9be5-851344629929
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICryptAttribute, ICryptAttribute interface [Security], InitializeFromObjectId method, ICryptAttribute::InitializeFromObjectId, InitializeFromObjectId method [Security], InitializeFromObjectId method [Security], ICryptAttribute interface, InitializeFromObjectId,ICryptAttribute.InitializeFromObjectId, certenroll/ICryptAttribute::InitializeFromObjectId, security.icryptattribute_initializefromobjectid_method
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
-	ICryptAttribute.InitializeFromObjectId
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICryptAttribute::InitializeFromObjectId method


## -description


The <b>InitializeFromObjectId</b> method initializes a cryptographic attribute by using an object identifier.


## -parameters




### -param pObjectId [in]

Pointer to an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface that contains the object identifier of the attribute.


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
The pointer to the <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



You must initialize the <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> object by calling the <a href="https://msdn.microsoft.com/dce84308-aecc-4841-88da-e948313b90b3">InitializeFromName</a> or <a href="https://msdn.microsoft.com/2bb2ee69-02c3-41b9-a67b-036c7154a44e">InitializeFromValue</a> methods before using it in this method. 




## -see-also




<a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 


---
UID: NF:certenroll.ICryptAttribute.InitializeFromValues
title: ICryptAttribute::InitializeFromValues
author: windows-sdk-content
description: Initializes a cryptographic attribute by using an IX509Attributes object.
old-location: security\icryptattribute_initializefromvalues_method.htm
old-project: SecCertEnroll
ms.assetid: 763fd244-173d-4b0b-8809-e98c18b8e5b5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICryptAttribute interface [Security],InitializeFromValues method, ICryptAttribute.InitializeFromValues, ICryptAttribute::InitializeFromValues, InitializeFromValues, InitializeFromValues method [Security], InitializeFromValues method [Security],ICryptAttribute interface, certenroll/ICryptAttribute::InitializeFromValues, security.icryptattribute_initializefromvalues_method
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
 - ICryptAttribute.InitializeFromValues
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICryptAttribute::InitializeFromValues


## -description


The <b>InitializeFromValues</b> method initializes a cryptographic attribute by using an <a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a> object.


## -parameters




### -param pAttributes [in]

Pointer to an <a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a> interface that contains the attribute collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <b>InitializeFromValues</b> method uses the first <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a> object in the collection.




## -see-also




<a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 


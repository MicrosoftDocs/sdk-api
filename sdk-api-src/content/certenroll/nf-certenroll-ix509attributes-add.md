---
UID: NF:certenroll.IX509Attributes.Add
title: IX509Attributes::Add
author: windows-sdk-content
description: Adds an IX509Attribute object to the collection.
old-location: security\ix509attributes_add_method.htm
tech.root: SecCertEnroll
ms.assetid: 769293d8-0ae0-419f-9399-3c501d700251
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Add, Add method [Security], Add method [Security],IX509Attributes interface, IX509Attributes interface [Security],Add method, IX509Attributes.Add, IX509Attributes::Add, certenroll/IX509Attributes::Add, security.ix509attributes_add_method
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
 - IX509Attributes.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Attributes::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a> object to the collection.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a> interface that represents the attribute to add to the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 


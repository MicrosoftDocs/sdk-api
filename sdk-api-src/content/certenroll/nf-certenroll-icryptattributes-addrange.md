---
UID: NF:certenroll.ICryptAttributes.AddRange
title: ICryptAttributes::AddRange
author: windows-sdk-content
description: Adds a range of ICryptAttribute objects to the collection. The attributes are contained in another ICryptAttributes collection.
old-location: security\icryptattributes_addrange_method.htm
tech.root: SecCertEnroll
ms.assetid: 8dc0a2c5-3734-47c7-a716-f53322fee39d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddRange, AddRange method [Security], AddRange method [Security],ICryptAttributes interface, ICryptAttributes interface [Security],AddRange method, ICryptAttributes.AddRange, ICryptAttributes::AddRange, certenroll/ICryptAttributes::AddRange, security.icryptattributes_addrange_method
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
 - ICryptAttributes.AddRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- ICryptAttributes.AddRange
: 
---

# ICryptAttributes::AddRange


## -description


The <b>AddRange</b> method adds a range of <a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a> objects to the collection. The attributes are contained in another <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> interface that contains the attribute collection to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 


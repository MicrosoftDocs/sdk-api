---
UID: NF:certenroll.ICryptAttributes.AddRange
title: ICryptAttributes::AddRange
author: windows-sdk-content
description: Adds a range of ICryptAttribute objects to the collection. The attributes are contained in another ICryptAttributes collection.
old-location: security\icryptattributes_addrange_method.htm
tech.root: seccertenroll
ms.assetid: 8dc0a2c5-3734-47c7-a716-f53322fee39d
ms.author: windowssdkdev
ms.date: 08/31/2018
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
---

# ICryptAttributes::AddRange


## -description


The <b>AddRange</b> method adds a range of <a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a> objects to the collection. The attributes are contained in another <a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a> collection.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a> interface that contains the attribute collection to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 


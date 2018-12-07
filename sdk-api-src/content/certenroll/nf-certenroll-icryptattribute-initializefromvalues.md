---
UID: NF:certenroll.ICryptAttribute.InitializeFromValues
title: ICryptAttribute::InitializeFromValues
author: windows-sdk-content
description: Initializes a cryptographic attribute by using an IX509Attributes object.
old-location: security\icryptattribute_initializefromvalues_method.htm
tech.root: seccertenroll
ms.assetid: 763fd244-173d-4b0b-8809-e98c18b8e5b5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICryptAttribute interface [Security],InitializeFromValues method, ICryptAttribute.InitializeFromValues, ICryptAttribute::InitializeFromValues, InitializeFromValues, InitializeFromValues method [Security], InitializeFromValues method [Security],ICryptAttribute interface, certenroll/ICryptAttribute::InitializeFromValues, security.icryptattribute_initializefromvalues_method
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
 - ICryptAttribute.InitializeFromValues
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICryptAttribute::InitializeFromValues


## -description


The <b>InitializeFromValues</b> method initializes a cryptographic attribute by using an <a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a> object.


## -parameters




### -param pAttributes [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a> interface that contains the attribute collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The <b>InitializeFromValues</b> method uses the first <a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a> object in the collection.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 


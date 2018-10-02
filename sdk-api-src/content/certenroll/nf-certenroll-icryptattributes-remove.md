---
UID: NF:certenroll.ICryptAttributes.Remove
title: ICryptAttributes::Remove
author: windows-sdk-content
description: Removes an ICryptAttribute object from the collection by index number.
old-location: security\icryptattributes_remove_method.htm
tech.root: SecCertEnroll
ms.assetid: 6e5767e0-41e8-4081-a814-263397a9faf9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICryptAttributes interface [Security],Remove method, ICryptAttributes.Remove, ICryptAttributes::Remove, Remove, Remove method [Security], Remove method [Security],ICryptAttributes interface, certenroll/ICryptAttributes::Remove, security.icryptattributes_remove_method
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
 - ICryptAttributes.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICryptAttributes::Remove


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375930(v=VS.85).aspx">ICryptAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 


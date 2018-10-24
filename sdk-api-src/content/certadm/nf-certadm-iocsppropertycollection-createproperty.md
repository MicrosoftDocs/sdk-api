---
UID: NF:certadm.IOCSPPropertyCollection.CreateProperty
title: IOCSPPropertyCollection::CreateProperty
author: windows-sdk-content
description: Creates a new property and adds it to a property set.
old-location: security\iocsppropertycollection_createproperty_method.htm
tech.root: SecCrypto
ms.assetid: 72e23a11-0550-47ae-9c24-90c1d18024a6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CreateProperty, CreateProperty method [Security], CreateProperty method [Security],IOCSPPropertyCollection interface, IOCSPPropertyCollection interface [Security],CreateProperty method, IOCSPPropertyCollection.CreateProperty, IOCSPPropertyCollection::CreateProperty, certadm/IOCSPPropertyCollection::CreateProperty, security.iocsppropertycollection_createproperty_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certadm.h
req.include-header: Certserv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPPropertyCollection.CreateProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCSPPropertyCollection::CreateProperty


## -description


The <b>CreateProperty</b> method creates a new property and adds it to a property set.


## -parameters




### -param bstrPropName [in]

A string that contains the name of the new property object.


### -param pVarPropValue [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>A pointer to the new property object.</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>The new property object.</td>
</tr>
</table>

### -param ppVal [out]

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa386391(v=VS.85).aspx">IOCSPProperty</a> interface for the newly created object.


## -returns



<h3>C++</h3>
If the method succeeds, it returns <b>S_OK</b>.


If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.



<h3>VB</h3>
An 
<a href="https://msdn.microsoft.com/en-us/library/Aa386391(v=VS.85).aspx">IOCSPProperty</a>
 interface for the newly created object.



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa386394(v=VS.85).aspx">IOCSPPropertyCollection</a>
 

 


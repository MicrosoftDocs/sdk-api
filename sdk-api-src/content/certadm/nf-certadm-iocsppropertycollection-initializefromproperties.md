---
UID: NF:certadm.IOCSPPropertyCollection.InitializeFromProperties
title: IOCSPPropertyCollection::InitializeFromProperties
author: windows-sdk-content
description: Creates a property set from the properties contained in an existing server configuration.
old-location: security\iocsppropertycollection_initializefromproperties_method.htm
old-project: SecCrypto
ms.assetid: e944af4e-80e4-470e-be04-770cf0f89871
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IOCSPPropertyCollection interface [Security],InitializeFromProperties method, IOCSPPropertyCollection.InitializeFromProperties, IOCSPPropertyCollection::InitializeFromProperties, InitializeFromProperties, InitializeFromProperties method [Security], InitializeFromProperties method [Security],IOCSPPropertyCollection interface, certadm/IOCSPPropertyCollection::InitializeFromProperties, security.iocsppropertycollection_initializefromproperties_method
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPPropertyCollection.InitializeFromProperties
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# IOCSPPropertyCollection::InitializeFromProperties


## -description


The <b>InitializeFromProperties</b> method creates a property set from the properties contained in an existing server configuration.


## -parameters




### -param pVarProperties [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
A pointer to an array that contains the property values. Each array element is a <b>VARIANT</b> array that contains the property name <b>BSTR</b> and a value <b>VARIANT</b>.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
An array that contains the property values. Each array element is a <b>Variant</b> array that contains the property name <b>String</b> and a value <b>Variant</b>.

</td>
</tr>
</table>

## -returns



<h3>VB</h3>
If the method succeeds, it returns <b>S_OK</b>.


If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

If the method returns <b>E_UNEXPECTED</b>, the array pointed to by the <i>pVarProperties</i> parameter contained duplicate properties.

If the method returns <b>DISP_E_ARRAYISLOCKED</b>, the array pointed to by the <i>pVarProperties</i> parameter is locked.




## -see-also




<a href="https://msdn.microsoft.com/8c700357-0cb4-4780-9ff1-ac57c46f9183">IOCSPPropertyCollection</a>
 

 


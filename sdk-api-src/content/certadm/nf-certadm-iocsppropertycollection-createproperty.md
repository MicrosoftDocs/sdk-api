---
UID: NF:certadm.IOCSPPropertyCollection.CreateProperty
title: IOCSPPropertyCollection::CreateProperty (certadm.h)
description: Creates a new property and adds it to a property set.
helpviewer_keywords: ["CreateProperty","CreateProperty method [Security]","CreateProperty method [Security]","IOCSPPropertyCollection interface","IOCSPPropertyCollection interface [Security]","CreateProperty method","IOCSPPropertyCollection.CreateProperty","IOCSPPropertyCollection::CreateProperty","certadm/IOCSPPropertyCollection::CreateProperty","security.iocsppropertycollection_createproperty_method"]
old-location: security\iocsppropertycollection_createproperty_method.htm
tech.root: security
ms.assetid: 72e23a11-0550-47ae-9c24-90c1d18024a6
ms.date: 12/05/2018
ms.keywords: CreateProperty, CreateProperty method [Security], CreateProperty method [Security],IOCSPPropertyCollection interface, IOCSPPropertyCollection interface [Security],CreateProperty method, IOCSPPropertyCollection.CreateProperty, IOCSPPropertyCollection::CreateProperty, certadm/IOCSPPropertyCollection::CreateProperty, security.iocsppropertycollection_createproperty_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPPropertyCollection::CreateProperty
 - certadm/IOCSPPropertyCollection::CreateProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPPropertyCollection.CreateProperty
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

A pointer to an <a href="/windows/desktop/api/certadm/nn-certadm-iocspproperty">IOCSPProperty</a> interface for the newly created object.

## -returns

<h3>C++</h3>
If the method succeeds, it returns <b>S_OK</b>.


If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.



<h3>VB</h3>
An 
<a href="/windows/desktop/api/certadm/nn-certadm-iocspproperty">IOCSPProperty</a>
 interface for the newly created object.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocsppropertycollection">IOCSPPropertyCollection</a>
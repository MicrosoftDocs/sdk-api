---
UID: NN:wcmconfig.IItemEnumerator
title: IItemEnumerator (wcmconfig.h)
author: windows-sdk-content
description: Enumerates the items of a collection of settings and attributes.
old-location: smi\iitemenumerator.htm
tech.root: SMI
ms.assetid: f43245f1-81d9-4b06-8f0c-d490618a99fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IItemEnumerator, IItemEnumerator interface [SMI], IItemEnumerator interface [SMI],described, smi.iitemenumerator, wcmconfig/IItemEnumerator
ms.topic: interface
f1_keywords: 
 - "wcmconfig/IItemEnumerator"
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - IItemEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IItemEnumerator interface


## -description


Enumerates the items of a collection of settings and attributes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IItemEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IItemEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IItemEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-iitemenumerator-current">Current</a>
</td>
<td align="left" width="63%">
Retrieves the item from the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-iitemenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position to the next item in the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-iitemenumerator-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the current item pointer to an undetermined position.

</td>
</tr>
</table> 


## -remarks



SMI and SMI collections are not thread-safe. Modifying a collection will not invalidate an enumerator. Further operations on the enumerator do not result in exceptions, and could encounter an enumerator in an inconsistent state.




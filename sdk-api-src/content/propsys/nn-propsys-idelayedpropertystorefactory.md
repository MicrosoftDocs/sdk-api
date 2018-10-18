---
UID: NN:propsys.IDelayedPropertyStoreFactory
title: IDelayedPropertyStoreFactory
author: windows-sdk-content
description: Exposes a method to create a specified IPropertyStore object in circumstances where property access is potentially slow.
old-location: shell\IDelayedPropertyStoreFactory.htm
tech.root: shell
ms.assetid: 855c9f10-9f40-4c60-a669-551fa51133f5
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IDelayedPropertyStoreFactory, IDelayedPropertyStoreFactory interface [Windows Shell], IDelayedPropertyStoreFactory interface [Windows Shell],described, _shell_IDelayedPropertyStoreFactory, propsys/IDelayedPropertyStoreFactory, shell.IDelayedPropertyStoreFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IDelayedPropertyStoreFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDelayedPropertyStoreFactory interface


## -description


Exposes a method to create a specified <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> object in circumstances where property access is potentially slow.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDelayedPropertyStoreFactory</b> interface inherits from <a href="https://msdn.microsoft.com/78ea822d-da8e-4883-b0eb-4277e7eb87a2">IPropertyStoreFactory</a>. <b>IDelayedPropertyStoreFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDelayedPropertyStoreFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26df5fec-2a21-454e-9539-877c00a4f8fb">GetDelayedPropertyStore</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> interface object, as specified.

</td>
</tr>
</table> 


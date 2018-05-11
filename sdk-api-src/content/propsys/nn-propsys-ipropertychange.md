---
UID: NN:propsys.IPropertyChange
title: IPropertyChange
author: windows-driver-content
description: Exposes a method that encapsulates a change to a single property.
old-location: properties\IPropertyChange.htm
old-project: properties
ms.assetid: 7bdc31d8-ba03-4010-8aa1-89701ebbf8cd
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IPropertyChange, IPropertyChange interface [Windows Properties], IPropertyChange interface [Windows Properties],described, _shell_IPropertyChange, properties.IPropertyChange, propsys/IPropertyChange, shell.IPropertyChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyChange
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyChange interface


## -description


Exposes a method that encapsulates a change to a single property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyChange</b> interface inherits from <a href="https://msdn.microsoft.com/238c3e39-62ba-4e97-9a15-19ad2e2d12e7">IObjectWithPropertyKey</a>. <b>IPropertyChange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyChange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyChange_ApplyToPropVariant">ApplyToPropVariant</a>
</td>
<td align="left" width="63%">
Applies a change to a property value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/238c3e39-62ba-4e97-9a15-19ad2e2d12e7">IObjectWithPropertyKey</a>



<a href="shell.PSCreateSimplePropertyChange">PSCreateSimplePropertyChange</a>
 

 


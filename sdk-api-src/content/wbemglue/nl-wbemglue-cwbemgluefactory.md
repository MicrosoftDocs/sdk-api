---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CWbemGlueFactory class


## -description


<p class="CCE_Message">[The <b>CWbemGlueFactory</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>CWbemGlueFactory</b> class is part of the WMI Provider Framework. The Provider Framework implements methods of this interface internally to create new instances of classes for the provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CWbemGlueFactory</b> class inherits from <a href="_com_iclassfactory">IClassFactory</a>. <b>CWbemGlueFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CWbemGlueFactory</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62cc28a8-6b0e-4ded-94e9-2ef3956cfd27">CWbemGlueFactory</a>
</td>
<td align="left" width="63%">
Constructor.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>CWbemGlueFactory</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>CreateInstance</b></td>
<td align="left" width="63%">
Implements the <a href="_com_iclassfactory_createinstance">IClassFactory::CreateInstance</a>  method to create an instance of a locator object to create an instance of a provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>LockServer</b></td>
<td align="left" width="63%">
Implements the <a href="_com_iclassfactory_lockserver">IClassFactory::LockServer</a>  method to increment and decrement the lock count on the DLL.

</td>
</tr>
</table> 


## -remarks



The destructor for the class is <b>CWbemGlueFactory::~CWbemGlueFactory.</b>




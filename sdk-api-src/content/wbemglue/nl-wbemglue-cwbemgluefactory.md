---
UID: NL:wbemglue.CWbemGlueFactory
title: CWbemGlueFactory
author: windows-sdk-content
description: The CWbemGlueFactory class is part of the WMI Provider Framework. The Provider Framework implements methods of this interface internally to create new instances of classes for the provider.
old-location: wmi\cwbemgluefactory.htm
old-project: WmiSdk
ms.assetid: 1287cb02-695a-47df-88f6-0d9dfd6b81af
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: "??1CWbemGlueFactory@@QAE@XZ, ??1CWbemGlueFactory@@QEAA@XZ, CWbemGlueFactory, CWbemGlueFactory class [Windows Management Instrumentation], CWbemGlueFactory class [Windows Management Instrumentation],described, wbemglue/CWbemGlueFactory, wmi.cwbemgluefactory"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: wbemglue.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WbemTimeout
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CWbemGlueFactory
-	CreateInstance
-	LockServer
-	??1CWbemGlueFactory@@QAE@XZ
-	??1CWbemGlueFactory@@QEAA@XZ
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
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




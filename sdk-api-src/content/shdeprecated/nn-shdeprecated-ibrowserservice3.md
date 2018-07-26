---
UID: NN:shdeprecated.IBrowserService3
title: IBrowserService3
author: windows-sdk-content
description: Deprecated.
old-location: shell\IBrowserService3.htm
old-project: shell
ms.assetid: efca41df-0aae-469e-8b56-77798eb8af19
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IBrowserService3, IBrowserService3 interface [Windows Shell], IBrowserService3 interface [Windows Shell],described, shdeprecated/IBrowserService3, shell.IBrowserService3, zone_IBrowserService3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BNSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.0
---

# IBrowserService3 interface


## -description


Deprecated. The methods exposed by this interface are analogous to virtual protected methods in normal C++ inheritance. The inheritance hierarchy of the objects spans multiple  DLLs. The hierarchy is made up of a base class and several derived classes that correspond to controls, including CLSID_WebBrowser and the user's desktop. Objects not in the hierarchy should not implement this interface, nor use most of its methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBrowserService3</b> interface inherits from <a href="https://msdn.microsoft.com/5c100b60-ef2e-4044-9f06-c1d01bcd88d2">IBrowserService2</a>. <b>IBrowserService3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBrowserService3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/310885e5-b08d-4699-9dee-244efa49dfd1">_PositionViewWindow</a>
</td>
<td align="left" width="63%">
Deprecated. Used in view size negotiations. This method is called by <a href="https://msdn.microsoft.com/92860c13-cb67-4499-90fe-2b0254ae25c7">_UpdateViewRectSize</a> after determining the available dimensions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e36418e-026b-4682-9074-4caec5370f8b">IEParseDisplayNameEx</a>
</td>
<td align="left" width="63%">
Deprecated. Parses a URL into a PIDL.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/e12ada84-0825-4946-8075-731dfc51ef50">IBrowserService</a> and <a href="https://msdn.microsoft.com/5c100b60-ef2e-4044-9f06-c1d01bcd88d2">IBrowserService2</a> interfaces, from which it inherits.




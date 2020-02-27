---
UID: NN:shdeprecated.IBrowserService3
title: IBrowserService3 (shdeprecated.h)
description: Deprecated.
old-location: shell\IBrowserService3.htm
tech.root: shell
ms.assetid: efca41df-0aae-469e-8b56-77798eb8af19
ms.date: 12/05/2018
ms.keywords: IBrowserService3, IBrowserService3 interface [Windows Shell], IBrowserService3 interface [Windows Shell],described, shdeprecated/IBrowserService3, shell.IBrowserService3, zone_IBrowserService3
f1_keywords:
- shdeprecated/IBrowserService3
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shdeprecated.h
api_name:
- IBrowserService3
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 6.0
ms.custom: 19H1
---

# IBrowserService3 interface


## -description


Deprecated. The methods exposed by this interface are analogous to virtual protected methods in normal C++ inheritance. The inheritance hierarchy of the objects spans multiple  DLLs. The hierarchy is made up of a base class and several derived classes that correspond to controls, including CLSID_WebBrowser and the user's desktop. Objects not in the hierarchy should not implement this interface, nor use most of its methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBrowserService3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nn-shdeprecated-ibrowserservice2">IBrowserService2</a>. <b>IBrowserService3</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice3-_positionviewwindow">_PositionViewWindow</a>
</td>
<td align="left" width="63%">
Deprecated. Used in view size negotiations. This method is called by <a href="https://docs.microsoft.com/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_updateviewrectsize">_UpdateViewRectSize</a> after determining the available dimensions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice3-ieparsedisplaynameex">IEParseDisplayNameEx</a>
</td>
<td align="left" width="63%">
Deprecated. Parses a URL into a PIDL.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nn-shdeprecated-ibrowserservice">IBrowserService</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nn-shdeprecated-ibrowserservice2">IBrowserService2</a> interfaces, from which it inherits.




---
UID: NN:shdeprecated.IExpDispSupport
title: IExpDispSupport (shdeprecated.h)
description: Deprecated. Exposes methods that allow the retrieval of properties, translation of keyboard accelerators, and determination of a connection point for certain events.helpviewer_keywords: ["IExpDispSupport","IExpDispSupport interface [Windows Shell]","IExpDispSupport interface [Windows Shell]","described","shdeprecated/IExpDispSupport","shell.IExpDispSupport","zone_IExpDispSupport"]
old-location: shell\IExpDispSupport.htm
tech.root: shell
ms.assetid: ddc71eaf-2c3a-4d70-80f1-6d499bf31b6d
ms.date: 12/05/2018
ms.keywords: IExpDispSupport, IExpDispSupport interface [Windows Shell], IExpDispSupport interface [Windows Shell],described, shdeprecated/IExpDispSupport, shell.IExpDispSupport, zone_IExpDispSupport
f1_keywords:
- shdeprecated/IExpDispSupport
dev_langs:
- c++
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
- IExpDispSupport
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# IExpDispSupport interface


## -description


Deprecated. Exposes methods that allow the retrieval of properties, translation of keyboard accelerators, and determination of a connection point for certain events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExpDispSupport</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExpDispSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExpDispSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-iexpdispsupport-findconnectionpoint">FindCIE4ConnectionPoint</a>
</td>
<td align="left" width="63%">
Deprecated. Gets connection points for browser events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-iexpdispsupport-oninvoke">OnInvoke</a>
</td>
<td align="left" width="63%">
Deprecated. Gets ambient properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-iexpdispsupport-ontranslateaccelerator">OnTranslateAccelerator</a>
</td>
<td align="left" width="63%">
Deprecated. Instructs the control site to process the keystroke described in <i>pMsg</i> and modified by the flags in <i>grfModifiers</i>.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  <b>IExpDispSupport</b> might not be supported in versions of Windows later than Windows XP.</div>
<div> </div>



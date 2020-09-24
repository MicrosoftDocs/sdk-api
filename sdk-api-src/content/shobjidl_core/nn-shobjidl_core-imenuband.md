---
UID: NN:shobjidl_core.IMenuBand
title: IMenuBand (shobjidl_core.h)
description: Exposes methods that allow a Component Object Model (COM) object to receive and translate appropriate messages.
helpviewer_keywords: ["IMenuBand","IMenuBand interface [Windows Shell]","IMenuBand interface [Windows Shell]","described","_shell_IMenuBand","shell.IMenuBand","shobjidl_core/IMenuBand"]
old-location: shell\IMenuBand.htm
tech.root: shell
ms.assetid: 67e12738-9951-4118-b968-7959cd175cf2
ms.date: 12/05/2018
ms.keywords: IMenuBand, IMenuBand interface [Windows Shell], IMenuBand interface [Windows Shell],described, _shell_IMenuBand, shell.IMenuBand, shobjidl_core/IMenuBand
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMenuBand
 - shobjidl_core/IMenuBand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IMenuBand
---

# IMenuBand interface


## -description

<p class="CCE_Message">[This interface is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be unsupported in subsequent versions of Windows.]

Exposes methods that allow a Component Object Model (COM) object to receive and translate appropriate messages.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMenuBand</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMenuBand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMenuBand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenuband-ismenumessage">IsMenuMessage</a>
</td>
<td align="left" width="63%">
A message pump calls this method to see if any messages should be redirected to the COM object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenuband-translatemenumessage">TranslateMenuMessage</a>
</td>
<td align="left" width="63%">
Translates a message for a COM object.

</td>
</tr>
</table>

## -remarks

 An application can call <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">QueryService</a> with one of the following service IDs. If the <i>riid</i> parameter of <b>QueryService</b> is IAccessible or IDispatch, the call to <b>QueryService</b> creates a new accessibility object. Otherwise, the call to <b>QueryService</b> is equivalent to a call to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> with the service ID, as follows:



<table class="clsStd">
<tr>
<th>Service ID (SID)</th>
<th>Meaning</th>
</tr>
<tr>
<td>SID_SMenuBandChild</td>
<td>Retrieves the pointer to the <b>IMenuBand</b> interface for the submenu.</td>
</tr>
<tr>
<td>SID_SMenuBandParent</td>
<td>Retrieves the pointer to the <b>IMenuBand</b> interface for the parent menu.</td>
</tr>
<tr>
<td>SID_SMenuBandTop</td>
<td>Retrieves the pointer to the <b>IMenuBand</b> interface for the top menu.</td>
</tr>
</table>
 

In Windows 2000, this interface was implemented in browseui.dll. However, it is not recommended that this version be used.
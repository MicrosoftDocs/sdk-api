---
UID: NN:shobjidl.ICommDlgBrowser3
title: ICommDlgBrowser3 (shobjidl.h)
description: Extends the capabilities of ICommDlgBrowser2, and used by the common file dialog boxes when they host a Shell browser.
old-location: shell\ICommDlgBrowser3.htm
tech.root: shell
ms.assetid: c9286061-8ac8-452b-9204-193bc6b571cb
ms.date: 12/05/2018
ms.keywords: ICommDlgBrowser3, ICommDlgBrowser3 interface [Windows Shell], ICommDlgBrowser3 interface [Windows Shell],described, _shell_ICommDlgBrowser3, shell.ICommDlgBrowser3, shobjidl/ICommDlgBrowser3
ms.topic: interface
f1_keywords:
- shobjidl/ICommDlgBrowser3
dev_langs:
- c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl.h
api_name:
- ICommDlgBrowser3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICommDlgBrowser3 interface


## -description


Extends the capabilities of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a>, and used by the common file dialog boxes when they host a Shell browser.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICommDlgBrowser3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a>. <b>ICommDlgBrowser3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICommDlgBrowser3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-icommdlgbrowser3-getcurrentfilter">GetCurrentFilter</a>
</td>
<td align="left" width="63%">
Gets the current filter as a Unicode string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-icommdlgbrowser3-oncolumnclicked">OnColumnClicked</a>
</td>
<td align="left" width="63%">
Called after a specified column is clicked in the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-icommdlgbrowser3-onpreviewcreated">OnPreViewCreated</a>
</td>
<td align="left" width="63%">
Called after a specified preview is created in the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser">ICommDlgBrowser</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a> interfaces, from which it inherits.

A pointer to <b>ICommDlgBrowser3</b> can be obtained by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a> object.




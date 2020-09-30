---
UID: NN:shobjidl.IFileDialog2
title: IFileDialog2 (shobjidl.h)
description: Extends the IFileDialog interface by providing methods that allow the caller to name a specific, restricted location that can be browsed in the common file dialog as well as to specify alternate text to display as a label on the Cancel button.
helpviewer_keywords: ["IFileDialog2","IFileDialog2 interface [Windows Shell]","IFileDialog2 interface [Windows Shell]","described","_shell_IFileDialog2","shell.IFileDialog2","shobjidl/IFileDialog2"]
old-location: shell\IFileDialog2.htm
tech.root: shell
ms.assetid: be67a020-285d-4c1e-a8b5-8e1e90fae594
ms.date: 12/05/2018
ms.keywords: IFileDialog2, IFileDialog2 interface [Windows Shell], IFileDialog2 interface [Windows Shell],described, _shell_IFileDialog2, shell.IFileDialog2, shobjidl/IFileDialog2
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileDialog2
 - shobjidl/IFileDialog2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comdlg32.dll
api_name:
 - IFileDialog2
---

# IFileDialog2 interface


## -description

Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> interface by providing methods that allow the caller to name a specific, restricted location that can be browsed in the common file dialog as well as to specify alternate text to display as a label on the <b>Cancel</b> button.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileDialog2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>. <b>IFileDialog2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileDialog2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl/nf-shobjidl-ifiledialog2-setcancelbuttonlabel">SetCancelButtonLabel</a>
</td>
<td align="left" width="63%">
Replaces the default text "Cancel" on the common file dialog's <b>Cancel</b> button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl/nf-shobjidl-ifiledialog2-setnavigationroot">SetNavigationRoot</a>
</td>
<td align="left" width="63%">
Specifies a top-level location from which to begin browsing a namespace, for instance in the <b>Save</b> dialog's <b>Browse folder</b> option. Users cannot navigate above this location.

</td>
</tr>
</table>

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided with Windows. Third parties do not provide custom implementations.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the methods of this interface in two instances:
            
                

<ul>
<li>When you want to restrict the dialog's navigation to a specific namespace.</li>
<li>When you need the dialog's <b>Cancel</b> button to be labeled differently in keeping with your functionality.</li>
</ul>
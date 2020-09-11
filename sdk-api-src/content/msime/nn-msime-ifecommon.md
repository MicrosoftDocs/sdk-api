---
UID: NN:msime.IFECommon
title: IFECommon (msime.h)
description: The IFECommon interface provides IME-related services that are common for different languages.
helpviewer_keywords: ["IFECommon","IFECommon interface [Internationalization for Windows Applications]","IFECommon interface [Internationalization for Windows Applications]","described","intl.ifecommon","msime/IFECommon"]
old-location: intl\ifecommon.htm
tech.root: Intl
ms.assetid: 9FBECA6F-F162-485D-938F-FADC2D47083E
ms.date: 12/05/2018
ms.keywords: IFECommon, IFECommon interface [Internationalization for Windows Applications], IFECommon interface [Internationalization for Windows Applications],described, intl.ifecommon, msime/IFECommon
req.header: msime.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFECommon
 - msime/IFECommon
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFECommon
---

# IFECommon interface


## -description

The <b>IFECommon</b> interface provides IME-related services that are common for different languages.

<b>IFECommon</b> allows the developer to control very basic functions of IMEs.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFECommon</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFECommon</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFECommon</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifecommon-invokedicttooldialog">InvokeDictToolDialog</a>
</td>
<td align="left" width="63%">
Invokes the Microsoft IME's Dictionary Tool from the app.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifecommon-invokewordregdialog">InvokeWordRegDialog</a>
</td>
<td align="left" width="63%">
Invokes the Microsoft IME Word Register Dialog Window from the app.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifecommon-isdefaultime">IsDefaultIME</a>
</td>
<td align="left" width="63%">
Determines if the IME specified by the class ID is the default IME on a local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifecommon-setdefaultime">SetDefaultIME</a>
</td>
<td align="left" width="63%">
Allows the Microsoft IME to become the default IME in the keyboard layout.

</td>
</tr>
</table>

## -remarks

Create an instance of this interface with the <a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-createifecommoninstance">CreateIFECommonInstance</a> function.


---
UID: NN:oleacc.IAccPropServices
title: IAccPropServices (oleacc.h)
author: windows-sdk-content
description: Exposes methods for annotating accessible elements and for manipulating identity strings.
old-location: winauto\iaccpropservices.htm
tech.root: WinAuto
ms.assetid: 0474dacf-7aa1-4d12-bac2-1091676a1ced
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAccPropServices, IAccPropServices interface [Windows Accessibility], IAccPropServices interface [Windows Accessibility],described, msaa.iaccpropservices, oleacc/IAccPropServices, winauto.iaccpropservices
ms.topic: interface
f1_keywords: 
 - "oleacc/IAccPropServices"
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oleacc.h
api_name:
 - IAccPropServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccPropServices interface


## -description


Exposes methods for annotating accessible elements and for manipulating identity strings. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccPropServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAccPropServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccPropServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearhwndprops">ClearHwndProps</a>
</td>
<td align="left" width="63%">
Restores default values to properties of <b>HWND</b>-based accessible elements that have been annotated previously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearprops">ClearProps</a>
</td>
<td align="left" width="63%">
Restores default values to properties of accessible elements that have been annotated previously. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring">ComposeHwndIdentityString</a>
</td>
<td align="left" width="63%">
Retrieves an identity string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-decomposehwndidentitystring">DecomposeHwndIdentityString</a>
</td>
<td align="left" width="63%">
Retrieves the <b>HWND</b>, object ID, and child ID for the accessible element identified by an identity string. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndprop">SetHwndProp</a>
</td>
<td align="left" width="63%">
Sets a new value for a property on an <b>HWND</b>-based object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropserver">SetHwndPropServer</a>
</td>
<td align="left" width="63%">
Specifies a callback object to be used to annotate an arrary of properties for an <b>HWND</b>-based accessible element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethwndpropstr">SetHwndPropStr</a>
</td>
<td align="left" width="63%">
Sets a new value for a string property on an <b>HWND</b>-based object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropserver">SetPropServer</a>
</td>
<td align="left" width="63%">
Specifies a callback object to be used to annotate an arrary of properties for the accessible element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropvalue">SetPropValue</a>
</td>
<td align="left" width="63%">
Sets a new value for a property.

</td>
</tr>
</table> 


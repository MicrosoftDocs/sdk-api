---
UID: NN:xamlom.IXamlDiagnostics
title: IXamlDiagnostics (xamlom.h)
description: Represents a XAML Diagnostics session.
old-location: xaml_diagnostics\ixamldiagnostics.htm
tech.root: xaml_diagnostics
ms.assetid: 1BCE3EC3-8B48-4F16-8E91-78776C07F309
ms.date: 12/05/2018
ms.keywords: IXamlDiagnostics, IXamlDiagnostics interface, IXamlDiagnostics interface,described, xaml_diagnostics.ixamldiagnostics, xamlom/IXamlDiagnostics
ms.topic: interface
f1_keywords:
- xamlom/IXamlDiagnostics
dev_langs:
- c++
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
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
- xamlom.h
api_name:
- IXamlDiagnostics
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXamlDiagnostics interface


## -description


Represents a XAML Diagnostics session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXamlDiagnostics</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXamlDiagnostics</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXamlDiagnostics</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ixamldiagnostics-getapplication">GetApplication</a>
</td>
<td align="left" width="63%">
Gets an instance of the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ixamldiagnostics-getdispatcher">GetDispatcher</a>
</td>
<td align="left" width="63%">
Gets the core dispatcher used to access elements on the UI thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ixamldiagnostics-gethandlefromiinspectable">GetHandleFromIInspectable</a>
</td>
<td align="left" width="63%">
Gets an <b>InstanceHandle</b> representation of an <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ixamldiagnostics-getiinspectablefromhandle">GetIInspectableFromHandle</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> from the XAML Diagnostics
    cache. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ixamldiagnostics-getinitializationdata">GetInitializationData</a>
</td>
<td align="left" width="63%">
Gets the initialization data passed in to XAML Diagnostics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ixamldiagnostics-getuilayer">GetUiLayer</a>
</td>
<td align="left" width="63%">
Gets the visual diagnostics root that can be used to draw
    on for highlighting elements in the tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ixamldiagnostics-hittest">HitTest</a>
</td>
<td align="left" width="63%">
Gets all elements in the visual tree that fall within the specified rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ixamldiagnostics-registerinstance">RegisterInstance</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> to the XAML Diagnostics cache and returns the newly created
    <b>InstanceHandle</b> for the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 


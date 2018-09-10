---
UID: NN:xamlom.IXamlDiagnostics
title: IXamlDiagnostics
author: windows-sdk-content
description: Represents a XAML Diagnostics session.
old-location: xaml_diagnostics\ixamldiagnostics.htm
tech.root: xaml_diagnostics
ms.assetid: 1BCE3EC3-8B48-4F16-8E91-78776C07F309
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IXamlDiagnostics, IXamlDiagnostics interface, IXamlDiagnostics interface,described, xaml_diagnostics.ixamldiagnostics, xamlom/IXamlDiagnostics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXamlDiagnostics interface


## -description


Represents a XAML Diagnostics session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXamlDiagnostics</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXamlDiagnostics</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/EA010DA4-2D13-41E9-B3E4-AD84AAF4E3FD">GetApplication</a>
</td>
<td align="left" width="63%">
Gets an instance of the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6C7605F7-BBD7-4FAD-AA35-A3DC18AA6FF3">GetDispatcher</a>
</td>
<td align="left" width="63%">
Gets the core dispatcher used to access elements on the UI thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/334497D9-11ED-4002-AEAB-0454EB62E53C">GetHandleFromIInspectable</a>
</td>
<td align="left" width="63%">
Gets an <b>InstanceHandle</b> representation of an <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F5BD99E0-CBAF-461C-9B4A-692604D4BAA9">GetIInspectableFromHandle</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> from the XAML Diagnostics
    cache. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D38409DC-7FB9-428D-B491-E2B5213224CF">GetInitializationData</a>
</td>
<td align="left" width="63%">
Gets the initialization data passed in to XAML Diagnostics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BE45AF9E-0C2D-439B-A360-2B9AE9359AEE">GetUiLayer</a>
</td>
<td align="left" width="63%">
Gets the visual diagnostics root that can be used to draw
    on for highlighting elements in the tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B7722F49-F477-4D24-9183-BC09A4A12730">HitTest</a>
</td>
<td align="left" width="63%">
Gets all elements in the visual tree that fall within the specified rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B1BD13CE-6B20-45D0-83E2-AB7E15BDA6FC">RegisterInstance</a>
</td>
<td align="left" width="63%">
Adds an <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> to the XAML Diagnostics cache and returns the newly created
    <b>InstanceHandle</b> for the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 


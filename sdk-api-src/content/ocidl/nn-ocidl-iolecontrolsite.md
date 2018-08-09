---
UID: NN:ocidl.IOleControlSite
title: IOleControlSite
author: windows-sdk-content
description: Provides the methods that enable a site object to manage each embedded control within a container.
old-location: com\iolecontrolsite.htm
old-project: com
ms.assetid: 8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOleControlSite, IOleControlSite interface [COM], IOleControlSite interface [COM],described, _ctrl_iolecontrolsite, com.iolecontrolsite, ocidl/IOleControlSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleControlSite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleControlSite interface


## -description


Provides the methods that enable a site object to manage each embedded control within a container. A site object provides <b>IOleControlSite</b> as well as other site interfaces such as <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a> and <a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>. When a control requires the services expressed through this interface, it will query one of the other client site interfaces for <b>IOleControlSite</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleControlSite</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IOleControlSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleControlSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66cfdf22-db2b-41d2-9854-d6bf70fbe146">GetExtendedControl</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IDispatch</b> pointer to the extended control that the container uses to wrap the real control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abd9a6c6-1551-4423-b1d6-f735159f6df4">LockInPlaceActive</a>
</td>
<td align="left" width="63%">
Indicates whether a control should remain in-place active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9e915c0-3443-4464-9e3e-e1fbfe37e838">OnControlInfoChanged</a>
</td>
<td align="left" width="63%">
Informs the container that the control's <a href="https://msdn.microsoft.com/3f22dc1d-554a-4dd1-a79a-121117f65caf">CONTROLINFO</a> structure has changed and that the container should call the control's <a href="https://msdn.microsoft.com/defb7509-e586-45a0-9e56-de9eba17f18e">IOleControl::GetControlInfo</a> for an update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22869326-2815-49cb-8d03-14dca5d45689">OnFocus</a>
</td>
<td align="left" width="63%">
Indicates whether the control managed by this control site has gained or lost the focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88421303-8f90-4ff3-90e4-74cb6d64a541">ShowPropertyFrame</a>
</td>
<td align="left" width="63%">
Instructs a container to display a property sheet for the control embedded in this site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7add062-4b42-43be-a982-c881c947f8f0">TransformCoords</a>
</td>
<td align="left" width="63%">
Converts coordinates expressed in <b>HIMETRIC</b> units (as is standard in OLE) to the units specified by the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4f9a6f7-bb0f-41d2-b1b8-7fda2dbee278">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Passes a keystroke to the control site for processing.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>



<a href="https://msdn.microsoft.com/ef85dce6-b680-4a72-9277-4cfdab27cbbc">IOleControl</a>



<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>
 

 


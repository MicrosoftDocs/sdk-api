---
UID: NN:ocidl.IOleControlSite
title: IOleControlSite (ocidl.h)
author: windows-sdk-content
description: Provides the methods that enable a site object to manage each embedded control within a container.
old-location: com\iolecontrolsite.htm
tech.root: com
ms.assetid: 8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOleControlSite, IOleControlSite interface [COM], IOleControlSite interface [COM],described, _ctrl_iolecontrolsite, com.iolecontrolsite, ocidl/IOleControlSite
ms.topic: interface
f1_keywords: 
 - "ocidl/IOleControlSite"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IOleControlSite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleControlSite interface


## -description


Provides the methods that enable a site object to manage each embedded control within a container. A site object provides <b>IOleControlSite</b> as well as other site interfaces such as <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> and <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>. When a control requires the services expressed through this interface, it will query one of the other client site interfaces for <b>IOleControlSite</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleControlSite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleControlSite</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-getextendedcontrol">GetExtendedControl</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IDispatch</b> pointer to the extended control that the container uses to wrap the real control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-lockinplaceactive">LockInPlaceActive</a>
</td>
<td align="left" width="63%">
Indicates whether a control should remain in-place active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-oncontrolinfochanged">OnControlInfoChanged</a>
</td>
<td align="left" width="63%">
Informs the container that the control's <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/ns-ocidl-controlinfo">CONTROLINFO</a> structure has changed and that the container should call the control's <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iolecontrol-getcontrolinfo">IOleControl::GetControlInfo</a> for an update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-onfocus">OnFocus</a>
</td>
<td align="left" width="63%">
Indicates whether the control managed by this control site has gained or lost the focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-showpropertyframe">ShowPropertyFrame</a>
</td>
<td align="left" width="63%">
Instructs a container to display a property sheet for the control embedded in this site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-transformcoords">TransformCoords</a>
</td>
<td align="left" width="63%">
Converts coordinates expressed in <b>HIMETRIC</b> units (as is standard in OLE) to the units specified by the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-translateaccelerator">TranslateAccelerator</a>
</td>
<td align="left" width="63%">
Passes a keystroke to the control site for processing.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iolecontrol">IOleControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>
 

 


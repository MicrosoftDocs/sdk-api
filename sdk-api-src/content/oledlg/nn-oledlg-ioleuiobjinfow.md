---
UID: NN:oledlg.IOleUIObjInfoW
title: IOleUIObjInfoW (oledlg.h)
description: Implemented by containers and used by the container's Object Properties dialog box and by the Convert dialog box.
old-location: com\ioleuiobjinfo.htm
tech.root: com
ms.assetid: 508dccb3-e98b-4f62-8bc3-98ca2b0d1349
ms.date: 12/05/2018
ms.keywords: IOleUIObjInfo, IOleUIObjInfo interface [COM], IOleUIObjInfo interface [COM],described, IOleUIObjInfoA, IOleUIObjInfoW, _ole_IOleUIObjInfo, com.ioleuiobjinfo, oledlg/IOleUIObjInfo
f1_keywords:
- oledlg/IOleUIObjInfo
dev_langs:
- c++
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- OleDlg.h
api_name:
- IOleUIObjInfo
- IOleUIObjInfoW
- IOleUIObjInfoA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleUIObjInfoW interface


## -description


Implemented by containers and used by the container's <b>Object Properties</b> dialog box and by the <b>Convert</b> dialog box. It provides information used by the <b>General</b> and <b>View</b> pages of the <b>Object Properties</b> dialog box , which display information about the object's size, location, type, and name. It also allows the object to be converted using the <b>Convert</b> dialog box. The <b>View</b> page allows the object's icon to be modified from its original form, and its display aspect to be changed (iconic versus content). Optionally, you can have your implementation of this interface allow the scale of the object to be changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleUIObjInfo</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>. <b>IOleUIObjInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleUIObjInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuiobjinfoa-convertobject">ConvertObject</a>
</td>
<td align="left" width="63%">
Converts the object to the type of the specified CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuiobjinfoa-getconvertinfo">GetConvertInfo</a>
</td>
<td align="left" width="63%">
Gets the conversion information associated with the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuiobjinfoa-getobjectinfo">GetObjectInfo</a>
</td>
<td align="left" width="63%">
Gets the size, type, name, and location information about an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuiobjinfoa-getviewinfo">GetViewInfo</a>
</td>
<td align="left" width="63%">
Gets the view information associated with the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-ioleuiobjinfoa-setviewinfo">SetViewInfo</a>
</td>
<td align="left" width="63%">
Sets the view information associated with the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-oleuiobjectpropertiesa">OleUIObjectProperties</a>
 

 


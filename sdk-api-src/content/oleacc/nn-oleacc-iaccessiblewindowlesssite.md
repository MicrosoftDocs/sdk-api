---
UID: NN:oleacc.IAccessibleWindowlessSite
title: IAccessibleWindowlessSite
author: windows-sdk-content
description: A Microsoft ActiveX control site implements this interface to enable a windowless ActiveX control that has a Microsoft Active Accessibility implementation to express its accessibility.
old-location: winauto\uiauto_IAccessibleWindowlessSite.htm
tech.root: WinAuto
ms.assetid: 1ED23B39-231B-46A2-9FED-969A36DA8DD9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAccessibleWindowlessSite, IAccessibleWindowlessSite interface [Windows Accessibility], IAccessibleWindowlessSite interface [Windows Accessibility],described, oleacc/IAccessibleWindowlessSite, winauto.uiauto_IAccessibleWindowlessSite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Oleacc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Oleacc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessibleWindowlessSite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibleWindowlessSite interface


## -description


A Microsoft ActiveX control site implements this interface to enable a windowless ActiveX control that has a Microsoft Active Accessibility implementation to express its accessibility.    This interface enables the control container to reserve a range of object IDs that a windowless control can use to raise events, and enables the control container to provide an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> pointer for the parent of the windowless control. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibleWindowlessSite</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAccessibleWindowlessSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibleWindowlessSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EB8BAD4D-0C8F-4926-A1B4-383D03C3B0C4">AcquireObjectIdRange</a>
</td>
<td align="left" width="63%">
Acquires a range of object IDs from the control host and marks them as reserved by a specific windowless control.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/579C2425-9C3E-4CFF-8A25-C661670FB636">GetParentAccessible</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> pointer for the parent of a windowless ActiveX control in the accessibility tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36663457-57B7-40D4-8A52-9C4E9B551E8E">QueryObjectIdRanges</a>
</td>
<td align="left" width="63%">
Retrieves the object ID ranges that a particular windowless ActiveX control has reserved.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CC7AEE46-88BE-445C-A377-C9E8C2B505D3">ReleaseObjectIdRange</a>
</td>
<td align="left" width="63%">
Releases an object ID range that was acquired by a previous call to the <a href="https://msdn.microsoft.com/EB8BAD4D-0C8F-4926-A1B4-383D03C3B0C4">IAccessibleWindowlessSite::AcquireObjectIdRange</a> method.

</td>
</tr>
</table> 


## -remarks



The functions that manage object ID ranges expect the site object to maintain a list of ranges that have already been reserved.  When the window that contains the ActiveX control receives a <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message with an <b>LPARAM</b> value (object ID) that is in a reserved range, the window should call the <a href="https://msdn.microsoft.com/c552b26a-a8db-42a1-85c9-9578230def74">IAccessibleHandler::AccessibleObjectFromID</a> method to get an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> object for that object ID.




## -see-also




<a href="https://msdn.microsoft.com/E6BE069B-C639-4578-9E5F-8CFE1267A847">IRawElementProviderWindowlessSite</a>
 

 


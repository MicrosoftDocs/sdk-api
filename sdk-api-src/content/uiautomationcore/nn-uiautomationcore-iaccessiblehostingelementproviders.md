---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IAccessibleHostingElementProviders interface


## -description


A Microsoft Active Accessibility object implements this interface when the object is the root of an accessibility tree that includes windowless Microsoft ActiveX controls that implement Microsoft UI Automation.  Because Microsoft Active Accessibility and UI Automation use different interfaces, this interface enables a client to discover the list of hosted windowless ActiveX controls that support  UI Automation in case the client needs to treat them differently.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibleHostingElementProviders</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAccessibleHostingElementProviders</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibleHostingElementProviders</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39A9665F-C2F3-48A2-A165-50AD3B82455F">GetEmbeddedFragmentRoots</a>
</td>
<td align="left" width="63%">
Retrieves the  Microsoft Active Accessibility providers of  all windowless ActiveX controls that have a UI Automation provider implementation, and are hosted in a Microsoft Active Accessibility object that implements the <b>IAccessibleHostingElementProviders</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/847F285F-F31D-486C-BBC7-DEED69505306">GetObjectIdForProvider</a>
</td>
<td align="left" width="63%">
Retrieves the object ID associated with a contained windowless ActiveX control that implements UI Automation.  

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2DBD5B1A-127A-4D71-8117-5FCCE653698C">IRawElementProviderHostingAccessibles</a>
 

 


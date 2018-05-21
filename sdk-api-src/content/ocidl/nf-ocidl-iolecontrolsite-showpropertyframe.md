---
UID: NF:ocidl.IOleControlSite.ShowPropertyFrame
title: IOleControlSite::ShowPropertyFrame
author: windows-driver-content
description: Instructs a container to display a property sheet for the control embedded in this site.
old-location: com\iolecontrolsite_showpropertyframe.htm
old-project: com
ms.assetid: 88421303-8f90-4ff3-90e4-74cb6d64a541
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IOleControlSite interface [COM],ShowPropertyFrame method, IOleControlSite.ShowPropertyFrame, IOleControlSite::ShowPropertyFrame, ShowPropertyFrame, ShowPropertyFrame method [COM], ShowPropertyFrame method [COM],IOleControlSite interface, _ctrl_iolecontrolsite_showpropertyframe, com.iolecontrolsite_showpropertyframe, ocidl/IOleControlSite::ShowPropertyFrame
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IOleControlSite.ShowPropertyFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOleControlSite::ShowPropertyFrame


## -description


Instructs a container to display a property sheet for the control embedded in this site.


## -parameters






## -returns



This method can return the standard return value E_OUTOFMEMORY, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The container does not need to show property pages itself.

</td>
</tr>
</table>
 




## -remarks



A control must always call this method in the container first when it intends to show its own property pages. Calling this method gives the container a chance to have those property pages work with the container's extended controls. The container may include its own property pages as well in such cases, which doesn't affect the control at all. If the container does not implement this method or if it returns a failure of any kind, the control can show its property pages directly. Otherwise, the container has shown the pages.




## -see-also




<a href="https://msdn.microsoft.com/8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9">IOleControlSite</a>
 

 


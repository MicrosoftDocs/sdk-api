---
UID: NF:oleidl.IOleClientSite.OnShowWindow
title: IOleClientSite::OnShowWindow
author: windows-driver-content
description: Notifies a container when an embedded object's window is about to become visible or invisible. This method does not apply to an object that is activated in place and therefore has no window separate from that of its container.
old-location: com\ioleclientsite_onshowwindow.htm
old-project: com
ms.assetid: 9185add8-02d1-4bf3-99ff-82f64ba12ef4
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IOleClientSite interface [COM],OnShowWindow method, IOleClientSite.OnShowWindow, IOleClientSite::OnShowWindow, OnShowWindow, OnShowWindow method [COM], OnShowWindow method [COM],IOleClientSite interface, _ole_ioleclientsite_onshowwindow, com.ioleclientsite_onshowwindow, oleidl/IOleClientSite::OnShowWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleClientSite.OnShowWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOleClientSite::OnShowWindow


## -description


Notifies a container when an embedded object's window is about to become visible or invisible. This method does not apply to an object that is activated in place and therefore has no window separate from that of its container.


## -parameters




### -param fShow [in]

Indicates whether an object's window is open (TRUE) or closed (FALSE).


## -returns



This method returns S_OK on success.




## -remarks



An embedded object calls <b>OnShowWindow</b> to keep its container informed when the object is open in a window. This window may or may not be currently visible to the end user. The container uses this information to shade the object's client site when the object is displayed in a window, and to remove the shading when the object is not. A shaded object, having received this notification, knows that it already has an open window and therefore can respond to being double-clicked by bringing this window quickly to the top, instead of launching its application in order to obtain a new one.




## -see-also




<a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>
 

 


---
UID: NF:ocidl.IQuickActivate.QuickActivate
title: IQuickActivate::QuickActivate
author: windows-sdk-content
description: Quick activates a control.
old-location: com\iquickactivate_quickactivate.htm
old-project: com
ms.assetid: 504cb272-da1c-4ffb-b4b1-fdf288901660
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IQuickActivate interface [COM],QuickActivate method, IQuickActivate.QuickActivate, IQuickActivate::QuickActivate, QuickActivate, QuickActivate method [COM], QuickActivate method [COM],IQuickActivate interface, _ctrl_iquickactivate_quickactivate, com.iquickactivate_quickactivate, ocidl/IQuickActivate::QuickActivate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IQuickActivate.QuickActivate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IQuickActivate::QuickActivate


## -description


Quick activates a control.


## -parameters




### -param pQaContainer [in]

A pointer to the <a href="https://msdn.microsoft.com/8f3975eb-7cd2-449f-92cc-2b8773d9f37e">QACONTAINER</a> structure containing information about the container.


### -param pQaControl [in, out]

A pointer to the <a href="https://msdn.microsoft.com/dd7ee4b1-2ad9-4ceb-b569-9988696760e8">QACONTROL</a> structure filled in by the control to return information about the control to the container. The container calling this method must reserve memory for this structure.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -remarks



If the control does not support <a href="https://msdn.microsoft.com/9b3e3b56-5055-4dfa-83e6-702578662463">IQuickActivate</a>, the container performs certain handshaking operations when it loads the control. The container calls certain interfaces on the control and the control, in turn, calls back to certain interfaces on the container's client site. First, the container creates the control object and calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to query for interfaces that it needs. Then, the container calls <a href="https://msdn.microsoft.com/6690b5a3-bada-496c-89cb-a9ae1fc9dfb0">IOleObject::SetClientSite</a> on the control, passing a pointer to its client site. Next, the control calls <b>QueryInterface</b> on this site, retrieving a pointer to additional necessary interfaces.

Using the <b>QuickActivate</b> method, the container passes a pointer to a <a href="https://msdn.microsoft.com/8f3975eb-7cd2-449f-92cc-2b8773d9f37e">QACONTAINER</a> structure. The structure contains pointers to interfaces which are needed by the control and the values of some ambient properties that the control may need. Upon return, the control passes a pointer to a <a href="https://msdn.microsoft.com/dd7ee4b1-2ad9-4ceb-b569-9988696760e8">QACONTROL</a> structure that contains pointers to its own interfaces that the container requires, and additional status information.

The <b>IPersist*::Load</b> and <b>IPersist*::InitNew</b> methods should be called after quick activation occurs. The control should establish its connections to the container's sinks during quick activation. However, these connections are not live until <b>IPersist*::Load</b> or <b>IPersist*::InitNew</b> has been called.





## -see-also




<a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a>



<a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a>



<a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>



<a href="https://msdn.microsoft.com/49c413b3-3523-4602-9ec1-19f4e0fe5651">IPersistStreamInit</a>



<a href="https://msdn.microsoft.com/9b3e3b56-5055-4dfa-83e6-702578662463">IQuickActivate</a>
 

 


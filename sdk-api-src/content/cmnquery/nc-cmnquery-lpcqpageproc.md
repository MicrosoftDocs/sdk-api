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

# LPCQPAGEPROC callback function


## -description


The <b>CQPageProc</b> callback function is called by the query dialog box to notify the query form extension of events that occur in a query page. A pointer to this function is supplied to the query dialog box in the <i>pPageProc</i> member of the <a href="https://msdn.microsoft.com/09e407a2-7a58-483d-8422-4ae40c05b742">CQPAGE</a> structure. <b>CQPageProc</b> is a placeholder for the query form extension-defined function name.


## -parameters




### -param pPage

Pointer to a <a href="https://msdn.microsoft.com/09e407a2-7a58-483d-8422-4ae40c05b742">CQPAGE</a> structure that contains data about a query page.


### -param hwnd

Contains the window handle of the query page.


### -param uMsg

Contains a value that identifies the event that this function is called for. This can be one of the <a href="messages_communicated_through_user_interfaces.htm">Common Query Page Messages</a>.


### -param wParam

Contains additional message data. The contents of this parameter depend on the value of the <i>uMsg</i> parameter.


### -param lParam

Contains additional message data. The content of this parameter depends on the value of the <i>uMsg</i> parameter.


## -returns



The return value is the result of the message  and depends on the value of the <i>uMsg</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/2b62c1aa-ace7-4083-8eb3-7c5c499762c9">CQAddPagesProc</a>



<a href="https://msdn.microsoft.com/09e407a2-7a58-483d-8422-4ae40c05b742">CQPAGE</a>



<a href="messages_communicated_through_user_interfaces.htm">Common Query Page Messages</a>



<a href="https://msdn.microsoft.com/797496fd-67db-4ec2-beec-224664d5d330">IQueryForm::AddPages</a>
 

 


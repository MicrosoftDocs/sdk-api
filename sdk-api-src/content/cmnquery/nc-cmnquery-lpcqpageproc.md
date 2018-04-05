---
UID: NC:cmnquery.LPCQPAGEPROC
title: LPCQPAGEPROC
author: windows-driver-content
description: Called by the query dialog box to notify the query form extension of events that occur in a query page.
old-location: ad\cqpageproc.htm
old-project: AD
ms.assetid: 11d40439-0877-4870-80f8-88026c448a32
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: CQPageProc, CQPageProc callback function [Active Directory], LPCQPAGEPROC, LPCQPAGEPROC callback function pointer [Active Directory], ad.cqpageproc, cmnquery/CQPageProc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: cmnquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SR_RESOURCE_TYPE_REPLICATED_PARTITION_INFO, *PSR_RESOURCE_TYPE_REPLICATED_PARTITION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Cmnquery.h
api_name:
-	LPCQPAGEPROC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# LPCQPAGEPROC callback


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
 

 


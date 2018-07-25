---
UID: NF:faxcomex.IFaxInboundRouting.GetMethods
title: IFaxInboundRouting::GetMethods
author: windows-sdk-content
description: The GetMethods method retrieves the ordered collection of all the inbound routing methods exposed by all the inbound routing extensions currently registered with the fax service.
old-location: fax\_mfax_faxinboundrouting_getmethods.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2x9v.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FaxInboundRouting object [Fax Service],GetMethods method, FaxInboundRouting.GetMethods, GetMethods, GetMethods method [Fax Service], GetMethods method [Fax Service],FaxInboundRouting object, IFaxInboundRouting.GetMethods, IFaxInboundRouting::GetMethods, _mfax_faxinboundrouting.getmethods, fax._mfax_faxinboundrouting_getmethods
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxInboundRouting.GetMethods
 - IFaxInboundRouting.GetMethods
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxInboundRouting::GetMethods


## -description


The <b>GetMethods</b> method retrieves the ordered collection of all the inbound routing methods exposed by all the inbound routing extensions currently registered with the fax service.


## -parameters




### -param pFaxInboundRoutingMethods






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/ms686674(v=VS.85).aspx">FaxInboundRoutingMethods</a>**</b>

A <a href="https://msdn.microsoft.com/library/ms686674(v=VS.85).aspx">FaxInboundRoutingMethods</a> object.




## -remarks



Order is based on the <a href="https://msdn.microsoft.com/library/ms686150(v=VS.85).aspx">Priority</a> property of each routing method. The priority is associated with the order in which the fax service calls the routing method when the service receives a fax job.

To use this method, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/library/ms684595(v=VS.85).aspx">FaxInboundRouting</a>



<a href="https://msdn.microsoft.com/library/ms693492(v=VS.85).aspx">Visual Basic Example</a>
 

 


---
UID: NF:faxcomex.IFaxInboundRouting.GetMethods
title: IFaxInboundRouting::GetMethods
author: windows-sdk-content
description: The IFaxInboundRouting::GetMethods method retrieves the ordered collection of all the inbound routing methods exposed by all the inbound routing extensions currently registered with the fax service.
old-location: fax\_mfax_faxinboundrouting_getmethods_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2x9v_cpp.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetMethods, GetMethods method [Fax Service], GetMethods method [Fax Service],IFaxInboundRouting interface, IFaxInboundRouting interface [Fax Service],GetMethods method, IFaxInboundRouting.GetMethods, IFaxInboundRouting::GetMethods, _mfax_faxinboundrouting.getmethods_cpp, fax._mfax_faxinboundrouting_getmethods_cpp, faxcomex/IFaxInboundRouting::GetMethods
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxInboundRouting.GetMethods
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxInboundRouting::GetMethods


## -description


The <b>IFaxInboundRouting::GetMethods</b> method retrieves the ordered collection of all the inbound routing methods exposed by all the inbound routing extensions currently registered with the fax service.


## -parameters




### -param pFaxInboundRoutingMethods






#### - ppFaxInboundRoutingMethods [out, retval]

Type: <b><a href="https://msdn.microsoft.com/5a19c7d9-f602-4271-a772-fdc61b73024f">IFaxInboundRoutingMethods</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/5a19c7d9-f602-4271-a772-fdc61b73024f">IFaxInboundRoutingMethods</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Order is based on the <a href="https://msdn.microsoft.com/23208ac4-68c8-4f62-b588-2d0a5575f87c">Priority</a> property of each routing method. The priority is associated with the order in which the fax service calls the routing method when the service receives a fax job.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/255706ba-cbbd-4dfa-a9da-95bdd90328b5">IFaxInboundRouting</a>



<a href="https://msdn.microsoft.com/cef24608-cab1-4090-aa94-3a1b76733e98">Visual Basic Example</a>
 

 


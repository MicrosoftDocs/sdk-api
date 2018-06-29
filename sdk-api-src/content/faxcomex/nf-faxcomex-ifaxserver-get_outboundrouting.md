---
UID: NF:faxcomex.IFaxServer.get_OutboundRouting
title: IFaxServer::get_OutboundRouting
author: windows-sdk-content
description: The OutboundRouting property creates a FaxOutboundRouting configuration object. The object permits users to configure outbound routing groups and rules.
old-location: fax\_mfax_faxserver_outboundrouting.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6y1z.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxServer object [Fax Service],OutboundRouting property, FaxServer.OutboundRouting, IFaxServer.get_OutboundRouting, IFaxServer::get_OutboundRouting, OutboundRouting property [Fax Service], OutboundRouting property [Fax Service],FaxServer object, _mfax_faxserver.outboundrouting, fax._mfax_faxserver_outboundrouting, get_OutboundRouting
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
 - FaxServer.OutboundRouting
 - IFaxServer.get_OutboundRouting
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxServer::get_OutboundRouting


## -description


The <b>OutboundRouting</b> property creates a <a href="https://msdn.microsoft.com/library/ms690136(v=VS.85).aspx">FaxOutboundRouting</a> configuration object. The object permits users to configure outbound routing groups and rules.

This property is read-only.


## -parameters


## -remarks



This property is not supported in Windows XP, and will return the error: <a href="https://msdn.microsoft.com/library/ms693490(v=VS.85).aspx">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/ms689109(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/library/ms689110(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/library/ms693408(v=VS.85).aspx">Visual Basic Example</a>
 

 


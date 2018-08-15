---
UID: NF:faxcomex.IFaxServer.get_OutboundRouting
title: IFaxServer::get_OutboundRouting
author: windows-sdk-content
description: The OutboundRouting property creates a FaxOutboundRouting configuration object. The object permits users to configure outbound routing groups and rules.
old-location: fax\_mfax_faxserver_outboundrouting.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6y1z.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxServer object [Fax Service],OutboundRouting property, FaxServer.OutboundRouting, IFaxServer.get_OutboundRouting, IFaxServer::get_OutboundRouting, OutboundRouting property [Fax Service], OutboundRouting property [Fax Service],FaxServer object, _mfax_faxserver.outboundrouting, fax._mfax_faxserver_outboundrouting, get_OutboundRouting
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.redist: 
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


The <b>OutboundRouting</b> property creates a <a href="https://msdn.microsoft.com/64ff05d6-6ebe-4155-96cd-7b925c979492">FaxOutboundRouting</a> configuration object. The object permits users to configure outbound routing groups and rules.

This property is read-only.


## -parameters


## -remarks



This property is not supported in Windows XP, and will return the error: <a href="https://msdn.microsoft.com/b5d59fec-2802-40bd-8ce4-748137f30fb2">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>. 




## -see-also




<a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>



<a href="https://msdn.microsoft.com/5a05df3b-c56b-4dfc-a0ee-7f1c2861e9ae">Visual Basic Example</a>
 

 


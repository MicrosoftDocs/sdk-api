---
UID: NF:faxcomex.IFaxOutboundRoutingRules.get__NewEnum
title: IFaxOutboundRoutingRules::get__NewEnum
author: windows-sdk-content
description: The IFaxOutboundRoutingRules::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the FaxOutboundRoutingRules collection.
old-location: fax\_mfax_ifaxoutboundroutingrules_get__newenum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_2a7h.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFaxOutboundRoutingRules interface [Fax Service],get__NewEnum method, IFaxOutboundRoutingRules.get__NewEnum, IFaxOutboundRoutingRules::get__NewEnum, _mfax_ifaxoutboundroutingrules_get__newenum, fax._mfax_ifaxoutboundroutingrules_get__newenum, faxcomex/IFaxOutboundRoutingRules::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxOutboundRoutingRules interface
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
 - IFaxOutboundRoutingRules.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutboundRoutingRules::get__NewEnum


## -description


The <b>IFaxOutboundRoutingRules::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a> collection.


## -parameters




### -param ppUnk






#### - pUnk [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680509.aspx">IUnknown</a>**</b>

 Receives an indirect pointer to the enumerator object <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680509.aspx">IUnknown</a> interface for this collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/bd059904-b5b6-4485-a64e-0beaa4de7379">IFaxOutboundRoutingRules</a>
 

 


---
UID: NF:faxcomex.IFaxOutboundRoutingGroups.get__NewEnum
title: IFaxOutboundRoutingGroups::get__NewEnum
author: windows-sdk-content
description: The IFaxOutboundRoutingGroups::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the FaxOutboundRoutingGroups collection.
old-location: fax\_mfax_ifaxoutboundroutinggroups_get__newenum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0i7h.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IFaxOutboundRoutingGroups interface [Fax Service],get__NewEnum method, IFaxOutboundRoutingGroups.get__NewEnum, IFaxOutboundRoutingGroups::get__NewEnum, _mfax_ifaxoutboundroutinggroups_get__newenum, fax._mfax_ifaxoutboundroutinggroups_get__newenum, faxcomex/IFaxOutboundRoutingGroups::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxOutboundRoutingGroups interface
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
 - IFaxOutboundRoutingGroups.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutboundRoutingGroups::get__NewEnum


## -description


The <b>IFaxOutboundRoutingGroups::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/library/ms689211(v=VS.85).aspx">FaxOutboundRoutingGroups</a> collection.


## -parameters




### -param ppUnk






#### - pUnk [out, retval]

Type: <b><a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a>**</b>

Receives an indirect pointer to the enumerator object's <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface for this collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/library/ms689212(v=VS.85).aspx">IFaxOutboundRoutingGroups</a>
 

 


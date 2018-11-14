---
UID: NF:faxcomex.IFaxInboundRoutingMethods.get__NewEnum
title: IFaxInboundRoutingMethods::get__NewEnum
author: windows-sdk-content
description: The IFaxInboundRoutingMethods::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the IFaxInboundRoutingMethods collection.
old-location: fax\_mfax_ifaxinboundroutingmethods_get__newenum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2z3h.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxInboundRoutingMethods interface [Fax Service],get__NewEnum method, IFaxInboundRoutingMethods.get__NewEnum, IFaxInboundRoutingMethods::get__NewEnum, _mfax_ifaxinboundroutingmethods_get__newenum, fax._mfax_ifaxinboundroutingmethods_get__newenum, faxcomex/IFaxInboundRoutingMethods::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxInboundRoutingMethods interface
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxInboundRoutingMethods.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxInboundRoutingMethods.get__NewEnum
: 
---

# IFaxInboundRoutingMethods::get__NewEnum


## -description


The <b>IFaxInboundRoutingMethods::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/en-us/library/ms686682(v=VS.85).aspx">IFaxInboundRoutingMethods</a> collection.


## -parameters




### -param ppUnk [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>**</b>

Address of a pointer to the enumerator object's <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface for the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In Microsoft Visual Basic, you do not need to use the <b>_NewEnum</b> property because it is automatically used in the implementation of <b>For Each ... Next</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686682(v=VS.85).aspx">IFaxInboundRoutingMethods</a>
 

 


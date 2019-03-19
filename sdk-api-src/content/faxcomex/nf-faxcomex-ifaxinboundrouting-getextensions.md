---
UID: NF:faxcomex.IFaxInboundRouting.GetExtensions
title: IFaxInboundRouting::GetExtensions (faxcomex.h)
author: windows-sdk-content
description: The GetExtensions method retrieves the collection of inbound routing extensions registered with the fax service.
old-location: fax\_mfax_faxinboundrouting_getextensions_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_80oj_cpp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetExtensions, GetExtensions method [Fax Service], GetExtensions method [Fax Service],IFaxInboundRouting interface, IFaxInboundRouting interface [Fax Service],GetExtensions method, IFaxInboundRouting.GetExtensions, IFaxInboundRouting::GetExtensions, _mfax_faxinboundrouting.getextensions_cpp, fax._mfax_faxinboundrouting_getextensions_cpp, faxcomex/IFaxInboundRouting::GetExtensions
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
 - IFaxInboundRouting.GetExtensions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxInboundRouting::GetExtensions


## -description


The <a href="https://msdn.microsoft.com/en-us/library/ms687088(v=VS.85).aspx">GetExtensions</a> method retrieves the collection of inbound routing extensions registered with the fax service.


## -parameters




### -param pFaxInboundRoutingExtensions [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms684901(v=VS.85).aspx">IFaxInboundRoutingExtensions</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms684901(v=VS.85).aspx">IFaxInboundRoutingExtensions</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684596(v=VS.85).aspx">IFaxInboundRouting</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693492(v=VS.85).aspx">Visual Basic Example</a>
 

 


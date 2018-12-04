---
UID: NF:faxcomex.IFaxInboundRouting.GetExtensions
title: IFaxInboundRouting::GetExtensions
author: windows-sdk-content
description: The GetExtensions method retrieves the collection of inbound routing extensions registered with the fax service.
old-location: fax\_mfax_faxinboundrouting_getextensions_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_80oj_cpp.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetExtensions, GetExtensions method [Fax Service], GetExtensions method [Fax Service],IFaxInboundRouting interface, IFaxInboundRouting interface [Fax Service],GetExtensions method, IFaxInboundRouting.GetExtensions, IFaxInboundRouting::GetExtensions, _mfax_faxinboundrouting.getextensions_cpp, fax._mfax_faxinboundrouting_getextensions_cpp, faxcomex/IFaxInboundRouting::GetExtensions
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
 - IFaxInboundRouting.GetExtensions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxInboundRouting::GetExtensions


## -description


The <a href="https://msdn.microsoft.com/ecd9a5bb-1624-4cfe-a2d9-b9a5ed722fc4">GetExtensions</a> method retrieves the collection of inbound routing extensions registered with the fax service.


## -parameters




### -param pFaxInboundRoutingExtensions [out, retval]

Type: <b><a href="https://msdn.microsoft.com/6daf0614-c0d4-42ba-96de-60f35a39aff1">IFaxInboundRoutingExtensions</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/6daf0614-c0d4-42ba-96de-60f35a39aff1">IFaxInboundRoutingExtensions</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/255706ba-cbbd-4dfa-a9da-95bdd90328b5">IFaxInboundRouting</a>



<a href="https://msdn.microsoft.com/cef24608-cab1-4090-aa94-3a1b76733e98">Visual Basic Example</a>
 

 


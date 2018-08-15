---
UID: NF:tapi3if.ITMultiTrackTerminal.CreateTrackTerminal
title: ITMultiTrackTerminal::CreateTrackTerminal
author: windows-sdk-content
description: The CreateTrackTerminal method creates a multitrack terminal that can handle a given media type or types and media direction.
old-location: tapi3\itmultitrackterminal_createtrackterminal.htm
old-project: tapi
ms.assetid: fe853de7-5a22-4b49-aca0-e2e2a8c3e1d7
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CreateTrackTerminal, CreateTrackTerminal method [TAPI 2.2], CreateTrackTerminal method [TAPI 2.2],ITMultiTrackTerminal interface, ITMultiTrackTerminal interface [TAPI 2.2],CreateTrackTerminal method, ITMultiTrackTerminal.CreateTrackTerminal, ITMultiTrackTerminal::CreateTrackTerminal, _tapi3_itmultitrackterminal_createtrackterminal, tapi3.itmultitrackterminal_createtrackterminal, tapi3if/ITMultiTrackTerminal::CreateTrackTerminal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMultiTrackTerminal.CreateTrackTerminal
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITMultiTrackTerminal::CreateTrackTerminal


## -description


The 
<b>CreateTrackTerminal</b> method creates a multitrack terminal that can handle a given media type or types and media direction.


## -parameters




### -param MediaType [in]

Bitwise ORed list of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a> required for the terminal.


### -param TerminalDirection [in]

The 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a> descriptor for the terminal.


### -param ppTerminal [out]

Pointer to the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface returned by <b>ITMultiTrackTerminal::CreateTrackTerminal</b>. The application must call <b>Release</b> on the 
<b>ITTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/c9e5d8a4-78a6-4449-9c11-c780e72ab925">ITMultiTrackTerminal</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 


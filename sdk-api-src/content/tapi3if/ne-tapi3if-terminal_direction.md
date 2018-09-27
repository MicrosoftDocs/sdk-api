---
UID: NE:tapi3if.TERMINAL_DIRECTION
title: TERMINAL_DIRECTION
author: windows-sdk-content
description: The TERMINAL_DIRECTION enumeration is used to describe the direction of the media stream with respect to the local computer or the directional capabilities of a terminal.
old-location: tapi3\terminal_direction.htm
tech.root: tapi
ms.assetid: 55ef9df3-1b85-439b-8ecb-28e5069390b9
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: TD_BIDIRECTIONAL, TD_CAPTURE, TD_MULTITRACK_MIXED, TD_NONE, TD_RENDER, TERMINAL_DIRECTION, TERMINAL_DIRECTION enumeration [TAPI 2.2], _tapi3_terminal_direction, tapi3.terminal_direction, tapi3if/TD_BIDIRECTIONAL, tapi3if/TD_CAPTURE, tapi3if/TD_MULTITRACK_MIXED, tapi3if/TD_NONE, tapi3if/TD_RENDER, tapi3if/TERMINAL_DIRECTION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - TERMINAL_DIRECTION
product: Windows
targetos: Windows
req.typenames: TERMINAL_DIRECTION
req.redist: 
---

# TERMINAL_DIRECTION enumeration


## -description


The 
<b>TERMINAL_DIRECTION</b> enumeration is used to describe the direction of the media stream with respect to the local computer or the directional capabilities of a terminal.


## -enum-fields




### -field TD_CAPTURE

The stream is captured on the local computer, and the data is sent out to the remote end of the connection. When applied to a terminal, this means it can originate a stream.


### -field TD_RENDER

The stream is arriving from the remote end of the connection. When applied to a terminal, this means it can render a stream.


### -field TD_BIDIRECTIONAL

The terminal can handle either capture or render streams.


### -field TD_MULTITRACK_MIXED

Different tracks on the multi-track terminal may travel in different directions. For example, one track may specify <b>TD_RENDER</b> and another may specify <b>TD_CAPTURE</b>.


### -field TD_NONE

The terminal direction is unknown or not initialized.


## -see-also




<a href="https://msdn.microsoft.com/196abe2a-d88d-4b2d-8867-4e6cc15dee33">ITStream::get_Direction</a>



<a href="https://msdn.microsoft.com/402cde43-6b2a-4e4e-bf46-97fcafb7574a">ITStreamControl::CreateStream</a>



<a href="https://msdn.microsoft.com/e0a69c3d-1780-4088-8249-961788dbf184">ITTerminal::get_Direction</a>



<a href="https://msdn.microsoft.com/a6590503-8c95-496d-a35a-1bbb34c728e1">ITTerminalManager::CreateDynamicTerminal</a>



<a href="https://msdn.microsoft.com/2a2a037a-753c-4dd4-b6ce-10b69f2e2421">ITTerminalSupport::CreateTerminal</a>



<a href="https://msdn.microsoft.com/aad3a566-eb95-402c-b26f-da6bd89e52ea">ITTerminalSupport::GetDefaultStaticTerminal</a>
 

 


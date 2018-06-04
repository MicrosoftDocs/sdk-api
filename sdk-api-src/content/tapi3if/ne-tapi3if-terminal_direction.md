---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 


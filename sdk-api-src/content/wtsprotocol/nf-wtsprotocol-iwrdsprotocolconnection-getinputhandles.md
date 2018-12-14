---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetInputHandles
title: IWRdsProtocolConnection::GetInputHandles
author: windows-sdk-content
description: Obtains the handles to input/output devices for the protocol.
old-location: termserv\iwrdsprotocolconnection_getinputhandles.htm
tech.root: TermServ
ms.assetid: 42f20dfc-e625-4b53-b055-750af4cbd3ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInputHandles, GetInputHandles method [Remote Desktop Services], GetInputHandles method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetInputHandles method, IWRdsProtocolConnection.GetInputHandles, IWRdsProtocolConnection::GetInputHandles, termserv.iwrdsprotocolconnection_getinputhandles, wtsprotocol/IWRdsProtocolConnection::GetInputHandles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
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
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnection.GetInputHandles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolConnection::GetInputHandles


## -description


Obtains the handles to input/output devices for the protocol.


## -parameters




### -param pKeyboardHandle [out]

A pointer to a handle that receives the handle of the keyboard device. This is a handle to an <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff539967(v=vs.85).aspx">I8042prt keyboard driver</a>.


### -param pMouseHandle [out]

A pointer to a handle that receives the handle of the mouse device. This is a handle to a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff542367(v=vs.85).aspx">Mouclass driver</a>.


### -param pBeepHandle [out]

A pointer to a handle that receives the handle of the beep or sound device. This handle is not used and must be set to <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 


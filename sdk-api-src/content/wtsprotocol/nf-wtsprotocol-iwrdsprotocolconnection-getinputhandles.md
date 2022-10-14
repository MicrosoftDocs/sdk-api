---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetInputHandles
title: IWRdsProtocolConnection::GetInputHandles (wtsprotocol.h)
description: Obtains the handles to input/output devices for the protocol.
helpviewer_keywords: ["GetInputHandles","GetInputHandles method [Remote Desktop Services]","GetInputHandles method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","GetInputHandles method","IWRdsProtocolConnection.GetInputHandles","IWRdsProtocolConnection::GetInputHandles","termserv.iwrdsprotocolconnection_getinputhandles","wtsprotocol/IWRdsProtocolConnection::GetInputHandles"]
old-location: termserv\iwrdsprotocolconnection_getinputhandles.htm
tech.root: TermServ
ms.assetid: 42f20dfc-e625-4b53-b055-750af4cbd3ec
ms.date: 12/05/2018
ms.keywords: GetInputHandles, GetInputHandles method [Remote Desktop Services], GetInputHandles method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetInputHandles method, IWRdsProtocolConnection.GetInputHandles, IWRdsProtocolConnection::GetInputHandles, termserv.iwrdsprotocolconnection_getinputhandles, wtsprotocol/IWRdsProtocolConnection::GetInputHandles
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsProtocolConnection::GetInputHandles
 - wtsprotocol/IWRdsProtocolConnection::GetInputHandles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnection.GetInputHandles
---

# IWRdsProtocolConnection::GetInputHandles


## -description

Obtains the handles to input/output devices for the protocol.

## -parameters

### -param pKeyboardHandle [out]

A pointer to a handle that receives the handle of the keyboard device. This is a handle to an <a href="/windows-hardware/drivers/ddi/content/index">I8042prt keyboard driver</a>.

### -param pMouseHandle [out]

A pointer to a handle that receives the handle of the mouse device. This is a handle to a <a href="/previous-versions/ff542367(v=vs.85)">Mouclass driver</a>.

### -param pBeepHandle [out]

A pointer to a handle that receives the handle of the beep or sound device. This handle is not used and must be set to <b>NULL</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>
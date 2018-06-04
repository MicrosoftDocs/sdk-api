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
 

 


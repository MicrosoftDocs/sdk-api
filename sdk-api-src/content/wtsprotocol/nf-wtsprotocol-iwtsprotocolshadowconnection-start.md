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

# IWTSProtocolShadowConnection::Start


## -description


<p class="CCE_Message">[<b>IWTSProtocolShadowConnection::Start</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/1f7b5811-6aba-41f2-9fa4-2bbc4c6e005c">IWRdsProtocolShadowConnection::Start</a>.]

Notifies the protocol that shadowing has started.


## -parameters




### -param pTargetServerName [in]

A pointer to a string that contains the name of the shadowing server.


### -param TargetSessionId [in]

An integer that specifies the ID of the target session to shadow.


### -param HotKeyVk [in]

The virtual key code of the key that must be pressed to stop shadowing. This key is used in combination with the <i>HotkeyModifiers</i> parameter.


### -param HotkeyModifiers [in]

The virtual modifier that specifies the modifier key to press to stop shadowing. Modifier keys include the Shift, Alt, and Ctrl keys. The modifier key is used in combination with the key signified by the <i>HotKeyVk</i> parameter.


### -param pShadowCallback [in]

A pointer to an <a href="https://msdn.microsoft.com/ce224b9f-161c-4133-97d9-05c339eefb77">IWTSProtocolShadowCallback</a> interface that the protocol can use to call back into the Remote Desktop Services service.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -remarks



The Remote Desktop Services service also changes the session state on the shadowed client to reflect the fact that it is being shadowed.




## -see-also




<a href="https://msdn.microsoft.com/83285a6a-903f-4c23-8f62-b04bbeaa52f9">IWTSProtocolShadowConnection</a>
 

 


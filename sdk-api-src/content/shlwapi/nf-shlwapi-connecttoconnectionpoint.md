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

# ConnectToConnectionPoint function


## -description


<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Establishes or terminates a connection between a client's sink and a connection point container.


## -parameters




### -param punk [in, optional]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the object to be connected to the connection point container. If you set <i>fConnect</i> to <b>FALSE</b> to indicate that you are disconnecting the object, this parameter is ignored and can be set to <b>NULL</b>.


### -param riidEvent [in]

Type: <b>REFIID</b>

The IID of the interface on the connection point container whose connection point object is being requested.


### -param fConnect

Type: <b>BOOL</b>

<b>TRUE</b> if a connection is being established; <b>FALSE</b> if a connection is being broken.


### -param punkTarget [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the connection point container's <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

A connection token. If you set <i>fConnect</i> to <b>TRUE</b> to make a new connection, this parameter receives a token that uniquely identifies the connection. If you set <i>fConnect</i> to <b>FALSE</b> to break a connection, this parameter must point to the token that you received when you called <b>ConnectToConnectionPoint</b> to establish the connection.


### -param ppcpOut [out, optional]

Type: <b><a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a>**</b>

A pointer to the connection point container's <a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a> interface, if the operation was successful. The calling application must release this pointer when it is no longer needed. If the request is unsuccessful, the pointer receives <b>NULL</b>. This parameter is optional and can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




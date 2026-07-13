---
UID: NF:shlwapi.ConnectToConnectionPoint
title: ConnectToConnectionPoint function (shlwapi.h)
description: Establishes or terminates a connection between a client's sink and a connection point container.
helpviewer_keywords: ["ConnectToConnectionPoint","ConnectToConnectionPoint function [Windows Shell]","_win32_ConnectToConnectionPoint","shell.ConnectToConnectionPoint","shlwapi/ConnectToConnectionPoint"]
old-location: shell\ConnectToConnectionPoint.htm
tech.root: shell
ms.assetid: f0c6051e-cced-4f38-a35d-d4c184d39084
ms.date: 12/05/2018
ms.keywords: ConnectToConnectionPoint, ConnectToConnectionPoint function [Windows Shell], _win32_ConnectToConnectionPoint, shell.ConnectToConnectionPoint, shlwapi/ConnectToConnectionPoint
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ShLwApi.Lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ConnectToConnectionPoint
 - shlwapi/ConnectToConnectionPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-IE-l1-1-0.dll
api_name:
 - ConnectToConnectionPoint
---

# ConnectToConnectionPoint function


## -description

<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Establishes or terminates a connection between a client's sink and a connection point container.

## -parameters

### -param punk [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the object to be connected to the connection point container. If you set <i>fConnect</i> to <b>FALSE</b> to indicate that you are disconnecting the object, this parameter is ignored and can be set to <b>NULL</b>.

### -param riidEvent [in]

Type: <b>REFIID</b>

The IID of the interface on the connection point container whose connection point object is being requested.

### -param fConnect

Type: <b>BOOL</b>

<b>TRUE</b> if a connection is being established; <b>FALSE</b> if a connection is being broken.

### -param punkTarget [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the connection point container's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

A connection token. If you set <i>fConnect</i> to <b>TRUE</b> to make a new connection, this parameter receives a token that uniquely identifies the connection. If you set <i>fConnect</i> to <b>FALSE</b> to break a connection, this parameter must point to the token that you received when you called <b>ConnectToConnectionPoint</b> to establish the connection.

### -param ppcpOut [out, optional]

Type: <b><a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>**</b>

A pointer to the connection point container's <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface, if the operation was successful. The calling application must release this pointer when it is no longer needed. If the request is unsuccessful, the pointer receives <b>NULL</b>. This parameter is optional and can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
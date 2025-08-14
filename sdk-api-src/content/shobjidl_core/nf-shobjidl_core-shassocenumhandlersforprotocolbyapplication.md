---
UID: NF:shobjidl_core.SHAssocEnumHandlersForProtocolByApplication
title: SHAssocEnumHandlersForProtocolByApplication function (shobjidl_core.h)
description: Gets an enumeration interface that provides access to handlers associated with a given protocol.
helpviewer_keywords: ["SHAssocEnumHandlersForProtocolByApplication","SHAssocEnumHandlersForProtocolByApplication function [Windows Shell]","_shell_SHAssocEnumHandlersForProtocolByApplication","shell.SHAssocEnumHandlersForProtocolByApplication","shobjidl_core/SHAssocEnumHandlersForProtocolByApplication"]
old-location: shell\SHAssocEnumHandlersForProtocolByApplication.htm
tech.root: shell
ms.assetid: 8bc3b9ce-5909-46a0-b5f1-35ab808aaa55
ms.date: 12/05/2018
ms.keywords: SHAssocEnumHandlersForProtocolByApplication, SHAssocEnumHandlersForProtocolByApplication function [Windows Shell], _shell_SHAssocEnumHandlersForProtocolByApplication, shell.SHAssocEnumHandlersForProtocolByApplication, shobjidl_core/SHAssocEnumHandlersForProtocolByApplication
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHAssocEnumHandlersForProtocolByApplication
 - shobjidl_core/SHAssocEnumHandlersForProtocolByApplication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-shell-associations-l1-1-3.dll
 - Shell32.dll
api_name:
 - SHAssocEnumHandlersForProtocolByApplication
---

# SHAssocEnumHandlersForProtocolByApplication function


## -description

Gets an enumeration interface that provides access to handlers associated with a given protocol.

## -parameters

### -param protocol [in]

Type: <b>PCWSTR</b>

Pointer to a string that specifies the protocol.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>enumHandlers</i>, typically IID_IEnumAssocHandlers.

### -param enumHandlers [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers">IEnumAssocHandlers</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is recommended that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>enumHandlers</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>enumHandlers</i>, which eliminates the possibility of a coding error.
---
UID: NF:shellapi.InitNetworkAddressControl
title: InitNetworkAddressControl function (shellapi.h)
description: Initializes the network address control window class.
helpviewer_keywords: ["InitNetworkAddressControl","InitNetworkAddressControl function [Windows Shell]","_shell_InitNetworkAddressControl","shell.InitNetworkAddressControl","shellapi/InitNetworkAddressControl"]
old-location: shell\InitNetworkAddressControl.htm
tech.root: shell
ms.assetid: 52b475e3-7335-4c34-80d7-ccd81af0e0ec
ms.date: 12/05/2018
ms.keywords: InitNetworkAddressControl, InitNetworkAddressControl function [Windows Shell], _shell_InitNetworkAddressControl, shell.InitNetworkAddressControl, shellapi/InitNetworkAddressControl
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OneCore.Lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitNetworkAddressControl
 - shellapi/InitNetworkAddressControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - InitNetworkAddressControl
---

# InitNetworkAddressControl function


## -description

Initializes the network address control window class.



## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the initialization succeeded; or <b>FALSE</b> otherwise.

## -remarks

The network address control looks like an edit control and offers the additional functionality of network address verification. The control uses a balloon tip to display error messages.

This function initializes class WC_NETADDRESS. If this function returns <b>TRUE</b>, the control can be created.


---
UID: NF:shellapi.InitNetworkAddressControl
title: InitNetworkAddressControl function
author: windows-sdk-content
description: Initializes the network address control window class.
old-location: shell\InitNetworkAddressControl.htm
tech.root: Shell
ms.assetid: 52b475e3-7335-4c34-80d7-ccd81af0e0ec
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: InitNetworkAddressControl, InitNetworkAddressControl function [Windows Shell], _shell_InitNetworkAddressControl, shell.InitNetworkAddressControl, shellapi/InitNetworkAddressControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - InitNetworkAddressControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitNetworkAddressControl function


## -description


Initializes the network address control window class.


## -parameters






## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the initialization succeeded; or <b>FALSE</b> otherwise.




## -remarks



The network address control looks like an edit control and offers the additional functionality of network address verification. The control uses a balloon tip to display error messages.

This function initializes class WC_NETADDRESS. If this function returns <b>TRUE</b>, the control can be created.




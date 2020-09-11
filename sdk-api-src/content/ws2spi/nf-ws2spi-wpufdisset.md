---
UID: NF:ws2spi.WPUFDIsSet
title: WPUFDIsSet function (ws2spi.h)
description: The WPUFDIsSet function checks the membership of the specified socket handle.
helpviewer_keywords: ["WPUFDIsSet","WPUFDIsSet function [Winsock]","_win32_wpufdisset_2","winsock.wpufdisset_2","ws2spi/WPUFDIsSet"]
old-location: winsock\wpufdisset_2.htm
tech.root: WinSock
ms.assetid: 87726b13-ede4-4c73-be98-4ad4180ea3e7
ms.date: 12/05/2018
ms.keywords: WPUFDIsSet, WPUFDIsSet function [Winsock], _win32_wpufdisset_2, winsock.wpufdisset_2, ws2spi/WPUFDIsSet
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WPUFDIsSet
 - ws2spi/WPUFDIsSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WPUFDIsSet
---

# WPUFDIsSet function


## -description

The 
**WPUFDIsSet** function checks the membership of the specified socket handle.

## -parameters

### -param s [in]

Descriptor identifying the socket.

### -param fdset [in]

Set to check for the membership of socket <i>s</i>.

## -returns

If no error occurs, a value of nonzero is returned denoting that socket <i>s</i> is a member of the <i>set</i> parameter. Otherwise, the return value is zero.

## -see-also

[LPWSPSelect](nc-ws2spi-lpwspselect.md)


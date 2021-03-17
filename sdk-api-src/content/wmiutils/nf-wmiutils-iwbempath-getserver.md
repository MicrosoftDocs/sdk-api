---
UID: NF:wmiutils.IWbemPath.GetServer
title: IWbemPath::GetServer (wmiutils.h)
description: The IWbemPath::GetServer method retrieves the server portion of the path.
helpviewer_keywords: ["GetServer","GetServer method [Windows Management Instrumentation]","GetServer method [Windows Management Instrumentation]","IWbemPath interface","IWbemPath interface [Windows Management Instrumentation]","GetServer method","IWbemPath.GetServer","IWbemPath::GetServer","_hmm_iwbempath_getserver","wmi.iwbempath_getserver","wmiutils/IWbemPath::GetServer"]
old-location: wmi\iwbempath_getserver.htm
tech.root: wmi
ms.assetid: 831d34d8-d586-41cc-a878-7a2b837b84de
ms.date: 12/05/2018
ms.keywords: GetServer, GetServer method [Windows Management Instrumentation], GetServer method [Windows Management Instrumentation],IWbemPath interface, IWbemPath interface [Windows Management Instrumentation],GetServer method, IWbemPath.GetServer, IWbemPath::GetServer, _hmm_iwbempath_getserver, wmi.iwbempath_getserver, wmiutils/IWbemPath::GetServer
req.header: wmiutils.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemPath::GetServer
 - wmiutils/IWbemPath::GetServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemPath.GetServer
---

# IWbemPath::GetServer


## -description

The 
<b>IWbemPath::GetServer</b> method retrieves the server portion of the path.

## -parameters

### -param puNameBufLength [in, out]

Upon input, this is the size in characters of the buffer pointed to by <i>pszName</i>. Upon return, this is the number of characters in the server name, including the <b>NULL</b> terminator.

### -param pName [in, out]

Server name.

## -returns

This method returns the following values.

## -remarks

This method can be used to determine how big a buffer is needed for <i>pszName</i>. This is done by passing in a <b>NULL</b> pointer for the buffer, setting <i>puNameBufLength</i> to 0 (zero) and then making the call. Upon return, <i>puNameBufLength</i> indicates how large a buffer is needed for <i>pszName</i> and its terminating <b>NULL</b> character.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>
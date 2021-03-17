---
UID: NF:ddeml.DdeQueryNextServer
title: DdeQueryNextServer function (ddeml.h)
description: Retrieves the next conversation handle in the specified conversation list.
helpviewer_keywords: ["DdeQueryNextServer","DdeQueryNextServer function [Data Exchange]","_win32_DdeQueryNextServer","_win32_ddequerynextserver_cpp","dataxchg.ddequerynextserver","ddeml/DdeQueryNextServer","winui._win32_ddequerynextserver"]
old-location: dataxchg\ddequerynextserver.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddequerynextserver.htm
ms.date: 12/05/2018
ms.keywords: DdeQueryNextServer, DdeQueryNextServer function [Data Exchange], _win32_DdeQueryNextServer, _win32_ddequerynextserver_cpp, dataxchg.ddequerynextserver, ddeml/DdeQueryNextServer, winui._win32_ddequerynextserver
req.header: ddeml.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdeQueryNextServer
 - ddeml/DdeQueryNextServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeQueryNextServer
---

# DdeQueryNextServer function


## -description

Retrieves the next conversation handle in the specified conversation list.

## -parameters

### -param hConvList [in]

Type: <b>HCONVLIST</b>

A handle to the conversation list. This handle must have been created by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnectlist">DdeConnectList</a> function.

### -param hConvPrev [in]

Type: <b>HCONV</b>

A handle to the conversation handle previously returned by this function. If this parameter is 0L, the function returns the first conversation handle in the list.

## -returns

Type: <b>HCONV</b>

If the list contains any more conversation handles, the return value is the next conversation handle in the list; otherwise, it is 0L.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnectlist">DdeConnectList</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddedisconnectlist">DdeDisconnectList</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
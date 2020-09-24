---
UID: NF:ddeml.DdeDisconnectList
title: DdeDisconnectList function (ddeml.h)
description: Destroys the specified conversation list and terminates all conversations associated with the list.
helpviewer_keywords: ["DdeDisconnectList","DdeDisconnectList function [Data Exchange]","_win32_DdeDisconnectList","_win32_ddedisconnectlist_cpp","dataxchg.ddedisconnectlist","ddeml/DdeDisconnectList","winui._win32_ddedisconnectlist"]
old-location: dataxchg\ddedisconnectlist.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddedisconnectlist.htm
ms.date: 12/05/2018
ms.keywords: DdeDisconnectList, DdeDisconnectList function [Data Exchange], _win32_DdeDisconnectList, _win32_ddedisconnectlist_cpp, dataxchg.ddedisconnectlist, ddeml/DdeDisconnectList, winui._win32_ddedisconnectlist
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
 - DdeDisconnectList
 - ddeml/DdeDisconnectList
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
 - DdeDisconnectList
---

# DdeDisconnectList function


## -description

Destroys the specified conversation list and terminates all conversations associated with the list.

## -parameters

### -param hConvList [in]

Type: <b>HCONVLIST</b>

A handle to the conversation list. This handle must have been created by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnectlist">DdeConnectList</a> function.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

An application can use the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddedisconnect">DdeDisconnect</a> function to terminate individual conversations in the list.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnect">DdeConnect</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnectlist">DdeConnectList</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddedisconnect">DdeDisconnect</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
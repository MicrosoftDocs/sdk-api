---
UID: NF:netsh.MatchEnumTag
title: MatchEnumTag function (netsh.h)
description: Searches a table of legal values to find a value that matches a specific token.
helpviewer_keywords: ["MatchEnumTag","MatchEnumTag function [NetShell]","_netsh_matchenumtag","netsh/MatchEnumTag","netshell.matchenumtag"]
old-location: netshell\matchenumtag.htm
tech.root: netshell
ms.assetid: def20f98-76a2-4d92-a954-152474e25f05
ms.date: 12/05/2018
ms.keywords: MatchEnumTag, MatchEnumTag function [NetShell], _netsh_matchenumtag, netsh/MatchEnumTag, netshell.matchenumtag
req.header: netsh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netsh.lib
req.dll: Netsh.exe
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MatchEnumTag
 - netsh/MatchEnumTag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netsh.exe
api_name:
 - MatchEnumTag
---

# MatchEnumTag function


## -description

The 
<b>MatchEnumTag</b> function searches a table of legal values to find a value that matches a specific token. The 
<b>MatchEnumTag</b> function is typically called by a command function when an argument is specified that has an enumerated set of possible values.

## -parameters

### -param hModule

Reserved. Set to null.

### -param pwcArg [in]

A token to match. The <i>pwcArg</i> parameter is usually an entry in the <i>ppwcArguments</i> array passed into the 
<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-fn_handle_cmd">FN_HANDLE_CMD</a> function exposed by the helper (the command function).

### -param dwNumArg [in]

The number of entries in the <i>pEnumTable</i> array.

### -param pEnumTable [in]

An array of token:value pairs.

### -param pdwValue [out]

Upon success, the <i>pdwValue</i> parameter is filled with the value associated with the token in the <i>pEnumTable</i> array.

## -see-also

<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-fn_handle_cmd">FN_HANDLE_CMD</a>
---
UID: NF:netsh.MatchToken
title: MatchToken function (netsh.h)
description: Determines whether a user-entered string matches a specific string.
helpviewer_keywords: ["MatchToken","MatchToken function [NetShell]","_netsh_matchtoken","netsh/MatchToken","netshell.matchtoken"]
old-location: netshell\matchtoken.htm
tech.root: netshell
ms.assetid: d6389d2e-1987-4ea6-967c-260686659852
ms.date: 12/05/2018
ms.keywords: MatchToken, MatchToken function [NetShell], _netsh_matchtoken, netsh/MatchToken, netshell.matchtoken
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
 - MatchToken
 - netsh/MatchToken
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
 - MatchToken
---

# MatchToken function


## -description

The 
<b>MatchToken</b> function determines whether a user-entered string matches a specific string. A match exists if the user-entered string is a case-insensitive prefix of the specific string.

## -parameters

### -param pwszUserToken [in]

A string entered by the user.

### -param pwszCmdToken [in]

A string against which to check for a match.

## -returns

Returns <b>TRUE</b> if there is a match, <b>FALSE</b> if not.

## -remarks

The 
<b>MatchToken</b> function is generally used by command functions. For arguments with an enumerated set of possible values, use the 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-matchenumtag">MatchEnumTag</a> function instead.

One example of using 
<b>MatchToken</b> is a command function that has an argument whose value can be an integer or the string "default". That command function might use 
<b>MatchToken</b> to test whether the value matches the string "default" before interpreting it as an integer.

## -see-also

<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-matchenumtag">MatchEnumTag</a>
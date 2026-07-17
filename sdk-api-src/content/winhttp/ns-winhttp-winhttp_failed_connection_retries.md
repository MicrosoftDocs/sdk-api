---
UID: NS:winhttp._WINHTTP_FAILED_CONNECTION_RETRIES
title: WINHTTP_FAILED_CONNECTION_RETRIES (winhttp.h)
description: Configures automatic retry behavior for failed connections when used with the WINHTTP_OPTION_FAILED_CONNECTION_RETRIES option flag.
prerelease: false
tech.root: http
ms.date: 03/25/2026
req.construct-type: structure
req.header: winhttp.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt:
req.target-min-winversvr:
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
req.typenames: WINHTTP_FAILED_CONNECTION_RETRIES, *PWINHTTP_FAILED_CONNECTION_RETRIES
req.redist:
f1_keywords:
 - WINHTTP_FAILED_CONNECTION_RETRIES
 - winhttp/WINHTTP_FAILED_CONNECTION_RETRIES
 - PWINHTTP_FAILED_CONNECTION_RETRIES
 - winhttp/PWINHTTP_FAILED_CONNECTION_RETRIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - WINHTTP_FAILED_CONNECTION_RETRIES
---

## -description

Configures automatic retry behavior for failed connections when used with the [**WINHTTP_OPTION_FAILED_CONNECTION_RETRIES**](/windows/win32/winhttp/option-flags) option flag. This structure specifies how many retries are allowed and under which conditions WinHTTP should retry a failed connection.

## -struct-fields

### -field dwMaxRetries

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The maximum number of retries allowed based on the retry conditions specified in *dwAllowedRetryConditions*.

### -field dwAllowedRetryConditions

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

A bitmask of values defining the retry conditions to be checked. This can be a combination of one or more of the following values.

| Value | Meaning |
|-------|---------|
| **WINHTTP_CONNECTION_RETRY_CONDITION_408** (0x1) | Retries if WinHTTP received a 408 (Request Timeout) response from the server. |
| **WINHTTP_CONNECTION_RETRY_CONDITION_SSL_HANDSHAKE** (0x2) | Retries on TLS/SSL handshake failures. |
| **WINHTTP_CONNECTION_RETRY_CONDITION_STALE_CONNECTION** (0x4) | Retries if a request send operation times out on a reused and stale connection. |

## -remarks

This structure is used with [**WinHttpSetOption**](/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption) when setting the [**WINHTTP_OPTION_FAILED_CONNECTION_RETRIES**](/windows/win32/winhttp/option-flags) option on a session handle. The option must be set on the session handle before any connection or request handles are created from that session.

The following code example shows how to set this option to retry up to 5 times on stale connection failures.

``` syntax
WINHTTP_FAILED_CONNECTION_RETRIES FailedConnectRetries;
FailedConnectRetries.dwMaxRetries = 5;
FailedConnectRetries.dwAllowedRetryConditions = WINHTTP_CONNECTION_RETRY_CONDITION_STALE_CONNECTION;

WinHttpSetOption(hSession,
                 WINHTTP_OPTION_FAILED_CONNECTION_RETRIES,
                 &FailedConnectRetries,
                 sizeof(FailedConnectRetries));
```

## -see-also

[**WINHTTP_OPTION_FAILED_CONNECTION_RETRIES**](/windows/win32/winhttp/option-flags)

[**WinHttpSetOption**](/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption)

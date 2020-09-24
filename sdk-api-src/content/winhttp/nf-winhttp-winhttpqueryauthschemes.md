---
UID: NF:winhttp.WinHttpQueryAuthSchemes
title: WinHttpQueryAuthSchemes function (winhttp.h)
description: The WinHttpQueryAuthSchemes function returns the authorization schemes that are supported by the server.
helpviewer_keywords: ["WINHTTP_AUTH_SCHEME_BASIC","WINHTTP_AUTH_SCHEME_DIGEST","WINHTTP_AUTH_SCHEME_NEGOTIATE","WINHTTP_AUTH_SCHEME_NTLM","WINHTTP_AUTH_SCHEME_PASSPORT","WINHTTP_AUTH_TARGET_PROXY","WINHTTP_AUTH_TARGET_SERVER","WinHttpQueryAuthSchemes","WinHttpQueryAuthSchemes function [WinHTTP]","http.winhttpqueryauthschemes","winhttp.winhttpqueryauthschemes_function","winhttp/WinHttpQueryAuthSchemes"]
old-location: http\winhttpqueryauthschemes.htm
tech.root: http
ms.assetid: 37fb9342-c5c2-46a3-a8b0-83060aa997e2
ms.date: 12/05/2018
ms.keywords: WINHTTP_AUTH_SCHEME_BASIC, WINHTTP_AUTH_SCHEME_DIGEST, WINHTTP_AUTH_SCHEME_NEGOTIATE, WINHTTP_AUTH_SCHEME_NTLM, WINHTTP_AUTH_SCHEME_PASSPORT, WINHTTP_AUTH_TARGET_PROXY, WINHTTP_AUTH_TARGET_SERVER, WinHttpQueryAuthSchemes, WinHttpQueryAuthSchemes function [WinHTTP], http.winhttpqueryauthschemes, winhttp.winhttpqueryauthschemes_function, winhttp/WinHttpQueryAuthSchemes
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - WinHttpQueryAuthSchemes
 - winhttp/WinHttpQueryAuthSchemes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpQueryAuthSchemes
---

# WinHttpQueryAuthSchemes function


## -description

The <b>WinHttpQueryAuthSchemes</b> function returns the authorization schemes that are supported by the server.

## -parameters

### -param hRequest [in]

Valid 
<a href="/windows/desktop/WinHttp/hinternet-handles-in-winhttp">HINTERNET</a> handle returned by 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopenrequest">WinHttpOpenRequest</a>

### -param lpdwSupportedSchemes [out]

An unsigned integer that specifies a flag that contains the supported authentication schemes.  This parameter can return one or more flags that are identified in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_BASIC"></a><a id="winhttp_auth_scheme_basic"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_BASIC</b></dt>
</dl>
</td>
<td width="60%">
Indicates basic authentication is available.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_NTLM"></a><a id="winhttp_auth_scheme_ntlm"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_NTLM</b></dt>
</dl>
</td>
<td width="60%">
Indicates NTLM authentication is available.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_PASSPORT"></a><a id="winhttp_auth_scheme_passport"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_PASSPORT</b></dt>
</dl>
</td>
<td width="60%">
Indicates passport authentication is available.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_DIGEST"></a><a id="winhttp_auth_scheme_digest"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_DIGEST</b></dt>
</dl>
</td>
<td width="60%">
Indicates digest authentication is available.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_NEGOTIATE"></a><a id="winhttp_auth_scheme_negotiate"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_NEGOTIATE</b></dt>
</dl>
</td>
<td width="60%">
Selects between NTLM and Kerberos authentication.

</td>
</tr>
</table>

### -param lpdwFirstScheme [out]

An unsigned integer that specifies a flag that contains the  first authentication scheme listed by the server.  This parameter can return one or more flags that are identified in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_BASIC"></a><a id="winhttp_auth_scheme_basic"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_BASIC</b></dt>
</dl>
</td>
<td width="60%">
Indicates basic authentication is first.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_NTLM"></a><a id="winhttp_auth_scheme_ntlm"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_NTLM</b></dt>
</dl>
</td>
<td width="60%">
Indicates NTLM authentication is first.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_PASSPORT"></a><a id="winhttp_auth_scheme_passport"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_PASSPORT</b></dt>
</dl>
</td>
<td width="60%">
Indicates passport authentication is first.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_DIGEST"></a><a id="winhttp_auth_scheme_digest"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_DIGEST</b></dt>
</dl>
</td>
<td width="60%">
Indicates digest authentication is first.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_SCHEME_NEGOTIATE"></a><a id="winhttp_auth_scheme_negotiate"></a><dl>
<dt><b>WINHTTP_AUTH_SCHEME_NEGOTIATE</b></dt>
</dl>
</td>
<td width="60%">
Selects between NTLM and Kerberos authentication.

</td>
</tr>
</table>

### -param pdwAuthTarget [out]

An unsigned integer that specifies a flag that contains the authentication target.  This parameter can return one or more flags that are identified in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_TARGET_SERVER"></a><a id="winhttp_auth_target_server"></a><dl>
<dt><b>WINHTTP_AUTH_TARGET_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Authentication target is a server. Indicates that a 401 status code has been received.

</td>
</tr>
<tr>
<td width="40%"><a id="WINHTTP_AUTH_TARGET_PROXY"></a><a id="winhttp_auth_target_proxy"></a><dl>
<dt><b>WINHTTP_AUTH_TARGET_PROXY</b></dt>
</dl>
</td>
<td width="60%">
Authentication target is a proxy. Indicates that a 407 status code has been received.

</td>
</tr>
</table>

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> if unsuccessful. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following table identifies the error codes that are returned.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of handle supplied is incorrect for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory was available to complete the requested operation. (Windows error code)

</td>
</tr>
</table>

## -remarks

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> is set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<b>WinHttpQueryAuthSchemes</b> cannot be used before calling 
<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryheaders">WinHttpQueryHeaders</a>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000 see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

The following example shows how to retrieve a specified document from an HTTP server when authentication is required.  The status code is retrieved from the response to determine if the server or proxy is requesting authentication.  If a 200 status code is found, the document is available. If a status code of 401 or 407 is found, authentication is required before the document can be retrieved.  For any other status code an error message is displayed.


```cpp
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient level
  //  of security to protect the server's resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  because Basic authentication exposes the client's username 
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset 
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or to 
    //  a redirect. If you don't, you can get into a 407-401-407-401
    //  loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE | 
                                          WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the contents 
          // of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(
           "The server requires authentication. Sending credentials\n");

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before re-sending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes );

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( 
                                        hRequest, dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check for
          // a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( 
           "The proxy requires authentication. Sending credentials\n");

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before re-sending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check for
          // a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf( "Error. Status code %d returned.\n", dwStatusCode );
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}


```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetcredentials">WinHttpSetCredentials</a>
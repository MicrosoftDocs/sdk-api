---
UID: NF:wininet.ResumeSuspendedDownload
title: ResumeSuspendedDownload function (wininet.h)
description: The ResumeSuspendedDownload function resumes a request that is suspended by a user interface dialog box.
helpviewer_keywords: ["ResumeSuspendedDownload","ResumeSuspendedDownload function [WinINet]","wininet.resumesuspendeddownload","wininet/ResumeSuspendedDownload"]
old-location: wininet\resumesuspendeddownload.htm
tech.root: wininet
ms.assetid: 72b5511a-872d-4058-9f38-9b1bdf6784c3
ms.date: 12/05/2018
ms.keywords: ResumeSuspendedDownload, ResumeSuspendedDownload function [WinINet], wininet.resumesuspendeddownload, wininet/ResumeSuspendedDownload
req.header: wininet.h
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
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResumeSuspendedDownload
 - wininet/ResumeSuspendedDownload
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - ResumeSuspendedDownload
---

# ResumeSuspendedDownload function


## -description

The <b>ResumeSuspendedDownload</b> function resumes a request that is suspended by a user interface dialog box.

## -parameters

### -param hRequest [in]

Handle of the request that is suspended by a user interface dialog box.

### -param dwResultCode [in]

The error result returned from <a href="/windows/desktop/api/wininet/nf-wininet-interneterrordlg">InternetErrorDlg</a>, or zero if a different dialog  is  invoked.

## -returns

Returns <b>TRUE</b> if successful; otherwise  <b>FALSE</b>. Call
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

## -remarks

Applications that use WinINet functions asynchronously can call <b>ResumeSuspendedDownload</b> to resume a request that is suspended by a user interface dialog box.

For example,  call  <b>ResumeSuspendedDownload</b> after a call to <a href="/windows/desktop/api/wininet/nf-wininet-interneterrordlg">InternetErrorDlg</a>, or in an <a href="/windows/desktop/api/wininet/nc-wininet-internet_status_callback">InternetStatusCallback</a>  function when the <i>lpvStatusInformation</i> parameter equals <b>INTERNET_STATUS_USER_INPUT_REQUIRED</b>. The following code example shows you how to use the <b>ResumeSuspendedDownload</b>  function in a callback.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

#### Examples


``` syntax
void CALLBACK YourInternetStatusCallbackFunction(
    HINTERNET hInternet,
    DWORD_PTR dwContext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation
    DWORD dwStatusInformationLength )
{
//  [...other callback code here]

  switch (dwInternetStatus)
  {
//  [...handle other INTERNET_STATUS cases]

    case INTERNET_STATUS_USER_INPUT_REQUIRED:
      ResumeSuspendedDownload( hInternet, 0 );
      break;

//  [...handle other INTERNET_STATUS cases]

    default:
//    [...default code]
      break;
  }

  return;
}
```


## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-interneterrordlg">InternetErrorDlg</a>



<a href="/windows/desktop/api/wininet/nc-wininet-internet_status_callback">InternetStatusCallback</a>

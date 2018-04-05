---
UID: NF:wininet.ResumeSuspendedDownload
title: ResumeSuspendedDownload function
author: windows-driver-content
description: The ResumeSuspendedDownload function resumes a request that is suspended by a user interface dialog box.
old-location: wininet\resumesuspendeddownload.htm
old-project: WinInet
ms.assetid: 72b5511a-872d-4058-9f38-9b1bdf6784c3
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ResumeSuspendedDownload, ResumeSuspendedDownload function [WinINet], wininet.resumesuspendeddownload, wininet/ResumeSuspendedDownload
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: InternetCookieState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wininet.dll
api_name:
-	ResumeSuspendedDownload
product: Windows
targetos: Windows
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ResumeSuspendedDownload function


## -description


The <b>ResumeSuspendedDownload</b> function resumes a request that is suspended by a user interface dialog box.


## -parameters




### -param hRequest [in]

Handle of the request that is suspended by a user interface dialog box.


### -param dwResultCode [in]

The error result returned from <a href="https://msdn.microsoft.com/09384ba9-e5cc-48fd-a52c-15df223f87dc">InternetErrorDlg</a>, or zero if a different dialog  is  invoked.


## -returns



Returns <b>TRUE</b> if successful; otherwise  <b>FALSE</b>. Call
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for extended error information.




## -remarks



Applications that use WinINet functions asynchronously can call <b>ResumeSuspendedDownload</b> to resume a request that is suspended by a user interface dialog box.

For example,  call  <b>ResumeSuspendedDownload</b> after a call to <a href="https://msdn.microsoft.com/09384ba9-e5cc-48fd-a52c-15df223f87dc">InternetErrorDlg</a>, or in an <a href="https://msdn.microsoft.com/a054fb71-66ab-46fd-be19-2237f05662bc">InternetStatusCallback</a>  function when the <i>lpvStatusInformation</i> parameter equals <b>INTERNET_STATUS_USER_INPUT_REQUIRED</b>. The following code example shows you how to use the <b>ResumeSuspendedDownload</b>  function in a callback.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

#### Examples

<pre class="syntax" xml:space="preserve"><code>void CALLBACK YourInternetStatusCallbackFunction(
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
}</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/09384ba9-e5cc-48fd-a52c-15df223f87dc">InternetErrorDlg</a>



<a href="https://msdn.microsoft.com/a054fb71-66ab-46fd-be19-2237f05662bc">InternetStatusCallback</a>
 

 


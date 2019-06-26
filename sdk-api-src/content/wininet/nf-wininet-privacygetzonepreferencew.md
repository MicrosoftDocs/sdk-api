---
UID: NF:wininet.PrivacyGetZonePreferenceW
title: PrivacyGetZonePreferenceW function (wininet.h)
author: windows-sdk-content
description: Retrieves the privacy settings for a given URLZONE and PrivacyType.
old-location: wininet\privacygetzonepreferencew.htm
tech.root: wininet
ms.assetid: 530a86a0-bb67-406a-be83-5f2b463a1aa1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PrivacyGetZonePreferenceW, PrivacyGetZonePreferenceW function [WinINet], wininet.privacygetzonepreferencew, winineti/PrivacyGetZonePreferenceW
ms.topic: function
f1_keywords: 
 - "wininet/PrivacyGetZonePreferenceW"
req.header: wininet.h
req.include-header: Wininet.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PrivacyGetZonePreferenceW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - PrivacyGetZonePreferenceW
 - PrivacyGetZonePreferenceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PrivacyGetZonePreferenceW function


## -description


Retrieves the privacy settings for a given 
<a href="https://docs.microsoft.com/dotnet/api/microsoft.visualstudio.ole.interop.urlzone?view=visualstudiosdk-2017">URLZONE</a> and <a href="https://docs.microsoft.com/windows/desktop/WinInet/privacy-type">PrivacyType</a>.


## -parameters




### -param dwZone [in]

A value of type <i>DWORD</i> that specifies the <a href="https://docs.microsoft.com/dotnet/api/microsoft.visualstudio.ole.interop.urlzone?view=visualstudiosdk-2017">URLZONE</a> for which privacy settings are being retrieved.


### -param dwType [in]

A value of type <i>DWORD</i> that specifies the <a href="https://docs.microsoft.com/windows/desktop/WinInet/privacy-type">PrivacyType</a> for which privacy settings are being retrieved.


### -param pdwTemplate [out, optional]

An <b>LPDWORD</b> that returns a pointer to a <b>DWORD</b> containing which of the <a href="https://docs.microsoft.com/windows/desktop/WinInet/privacy-templates">PrivacyTemplates</a> is in use for this <i>dwZone</i> and <i>dwType</i>.


### -param pszBuffer [out, optional]

An  <b>LPWSTR</b> that points to a buffer containing a <b>LPCWSTR</b> representing a string version of the <i>pdwTemplate</i> or a customized string if the <i>pdwTemplate</i> is set to <b>PRIVACY_TEMPLATE_CUSTOM</b>. See <a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-privacysetzonepreferencew">PrivacySetZonePreferenceW</a> for a description of a customized privacy preferences string.


### -param pdwBufferLength [in, out, optional]

An <b>LPDWORD</b> that contains the buffer length in characters. If the buffer length is not sufficient, <b>PrivacyGetZonePreferenceW</b> returns with this parameter set to the number of characters required and with a return value of <b>ERROR_MORE_DATA</b>.


## -returns



Returns zero if successful. Otherwise, one of the Error Messages defined in winerr.h is returned.




## -remarks



These privacy settings for the Internet zone are found on the Privacy tab of the Internet Options dialog box.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://docs.microsoft.com/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetclearallpersitecookiedecisions">InternetClearAllPerSiteCookieDecisions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetenumpersitecookiedecisiona">InternetEnumPerSiteCookieDecision</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetgetpersitecookiedecisiona">InternetGetPerSiteCookieDecision</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-internetsetpersitecookiedecisiona">InternetSetPerSiteCookieDecisions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wininet/nf-wininet-privacysetzonepreferencew">PrivacySetZonePreferenceW</a>
 

 


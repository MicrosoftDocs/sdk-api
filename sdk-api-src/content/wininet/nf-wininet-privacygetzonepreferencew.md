---
UID: NF:wininet.PrivacyGetZonePreferenceW
title: PrivacyGetZonePreferenceW function
author: windows-sdk-content
description: Retrieves the privacy settings for a given URLZONE and PrivacyType.
old-location: wininet\privacygetzonepreferencew.htm
old-project: wininet
ms.assetid: 530a86a0-bb67-406a-be83-5f2b463a1aa1
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: PrivacyGetZonePreferenceW, PrivacyGetZonePreferenceW function [WinINet], wininet.privacygetzonepreferencew, winineti/PrivacyGetZonePreferenceW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: InternetCookieState
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
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PrivacyGetZonePreferenceW function


## -description


Retrieves the privacy settings for a given 
<a href="https://msdn.microsoft.com/63ca4584-c714-4409-ab45-0500bdad6bd1">URLZONE</a> and <a href="https://msdn.microsoft.com/7d0846d4-fd81-4af9-b7e6-05c4c1438770">PrivacyType</a>.


## -parameters




### -param dwZone [in]

A value of type <i>DWORD</i> that specifies the <a href="https://msdn.microsoft.com/63ca4584-c714-4409-ab45-0500bdad6bd1">URLZONE</a> for which privacy settings are being retrieved.


### -param dwType [in]

A value of type <i>DWORD</i> that specifies the <a href="https://msdn.microsoft.com/7d0846d4-fd81-4af9-b7e6-05c4c1438770">PrivacyType</a> for which privacy settings are being retrieved.


### -param pdwTemplate [out, optional]

An <b>LPDWORD</b> that returns a pointer to a <b>DWORD</b> containing which of the <a href="https://msdn.microsoft.com/d8dd9c12-b159-4f95-820e-521aeb1526bf">PrivacyTemplates</a> is in use for this <i>dwZone</i> and <i>dwType</i>.


### -param pszBuffer [out, optional]

An  <b>LPWSTR</b> that points to a buffer containing a <b>LPCWSTR</b> representing a string version of the <i>pdwTemplate</i> or a customized string if the <i>pdwTemplate</i> is set to <b>PRIVACY_TEMPLATE_CUSTOM</b>. See <a href="https://msdn.microsoft.com/29c8dbc0-052e-40f4-a036-cb647d920055">PrivacySetZonePreferenceW</a> for a description of a customized privacy preferences string.


### -param pdwBufferLength [in, out, optional]

An <b>LPDWORD</b> that contains the buffer length in characters. If the buffer length is not sufficient, <b>PrivacyGetZonePreferenceW</b> returns with this parameter set to the number of characters required and with a return value of <b>ERROR_MORE_DATA</b>.


## -returns



Returns zero if successful. Otherwise, one of the Error Messages defined in winerr.h is returned.




## -remarks




These privacy settings for the Internet zone are found on the Privacy tab of the Internet Options dialog box.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/980df63e-70b8-44d3-b98a-b7c8a3e395c6">InternetClearAllPerSiteCookieDecisions</a>



<a href="https://msdn.microsoft.com/de1db7e6-21f4-4bbb-b4fc-277bbd01f32c">InternetEnumPerSiteCookieDecision</a>



<a href="https://msdn.microsoft.com/04fa4c33-077c-4b16-8170-c3770783c98a">InternetGetPerSiteCookieDecision</a>



<a href="https://msdn.microsoft.com/c25699b9-f79a-443b-b9a4-461c379fa8e4">InternetSetPerSiteCookieDecisions</a>



<a href="https://msdn.microsoft.com/29c8dbc0-052e-40f4-a036-cb647d920055">PrivacySetZonePreferenceW</a>
 

 


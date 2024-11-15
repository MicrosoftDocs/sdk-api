---
UID: NF:winineti.PrivacySetZonePreferenceW
title: PrivacySetZonePreferenceW function (winineti.h)
description: The PrivacySetZonePreferenceW function (winineti.h) sets the privacy settings for a given URLZONE and PrivacyType.
helpviewer_keywords: ["PrivacySetZonePreferenceW","PrivacySetZonePreferenceW function [WinINet]","wininet.privacysetzonepreferencew","winineti/PrivacySetZonePreferenceW"]
old-location: wininet\privacysetzonepreferencew.htm
tech.root: wininet
ms.assetid: 29c8dbc0-052e-40f4-a036-cb647d920055
ms.date: 08/15/2022
ms.keywords: PrivacySetZonePreferenceW, PrivacySetZonePreferenceW function [WinINet], wininet.privacysetzonepreferencew, winineti/PrivacySetZonePreferenceW
req.header: winineti.h
req.include-header: Wininet.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PrivacySetZonePreferenceW (Unicode)
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
 - PrivacySetZonePreferenceW
 - winineti/PrivacySetZonePreferenceW
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
 - PrivacySetZonePreferenceW
 - PrivacySetZonePreferenceW
---

# PrivacySetZonePreferenceW function


## -description

Sets the privacy settings for a given <a href="/dotnet/api/microsoft.visualstudio.ole.interop.urlzone">URLZONE</a> and <a href="/windows/desktop/WinInet/privacy-type">PrivacyType</a>.

## -parameters

### -param dwZone [in]

Value of type <b>DWORD</b> that specifies the <a href="/dotnet/api/microsoft.visualstudio.ole.interop.urlzone">URLZONE</a> for which privacy settings are being set.

### -param dwType [in]

Value of type <b>DWORD</b> that specifies the <a href="/windows/desktop/WinInet/privacy-type">PrivacyType</a> for which privacy settings are being set.

### -param dwTemplate [in]

Value of type <b>DWORD</b> that specifies which of the <a href="/windows/desktop/WinInet/privacy-templates">privacy templates</a> is to be used to set the privacy settings.

### -param pszPreference [in, optional]

If <i>dwTemplate</i> is set to <b>PRIVACY_TEMPLATE_CUSTOM</b>, this parameter is the string representation of the custom preferences. Otherwise, it should be set to <b>NULL</b>. A description of this string representation is included in the Remarks section.

## -returns

Returns zero if successful. Otherwise, one of the errors defined in winerr.h is returned.

## -remarks

These privacy settings for the Internet zone are found on the <b>Privacy</b> tab of the <b>Internet Options</b> dialog box.

Setting the privacy options for the <a href="/dotnet/api/microsoft.visualstudio.ole.interop.urlzone">URLZONE_INTERNET</a> involves setting the <a href="/windows/desktop/WinInet/privacy-templates">privacy templates</a> for both <a href="/windows/desktop/WinInet/privacy-type">PrivacyTypes</a>. The slider on the <b>Privacy</b> Menu in <b>Internet Options</b> only moves if privacy is set for both <b>PrivacyTypes</b>.

Custom privacy preferences for a given <a href="/dotnet/api/microsoft.visualstudio.ole.interop.urlzone">URLZONE</a> and <a href="/windows/desktop/WinInet/privacy-type">PrivacyType</a> can be set through the <i>pszPreference</i> parameter. The <i>pszPreference</i> parameter can contain a series of rules separated by white space describing the privacy preferences. It is important to note that the rules themselves cannot contain white space. The <i>pszPreference</i> has the following structure where there can be multiple logical rules: &lt;<i>signature</i>&gt; &lt;<i>logical-rule</i>&gt; &lt;<i>special-rule</i>&gt;.

Currently, the signature must be set to IE6-P3PSettings/V1:.

Logical rules have the following format: /&lt;<i>expression</i>&gt;=&lt;<i>decision</i>&gt;/.

An expression is a Boolean statement composed of compact policy tokens using the operators &amp; (logical AND) and ! (logical NOT). The compact policy token is case-sensitive. (For more information on Platform for Privacy Preferences (P3P) privacy policies and compact policy tokens, see the <a href="https://www.w3.org/P3P/">W3C: Platform for Privacy Preferences (P3P) Project</a>  specification.) The decision is a single lowercase character that defines the action to take on the cookie whose compact policy contains the specified token(s). The following table lists valid decision characters.

<table>
<tr>
<th>Character</th>
<th>Definition</th>
</tr>
<tr>
<td>a</td>
<td>Accept the cookie.</td>
</tr>
<tr>
<td>p</td>
<td>Prompt user to accept or deny the cookie.</td>
</tr>
<tr>
<td>r</td>
<td>Reject the cookie.</td>
</tr>
<tr>
<td>l</td>
<td>Leash the cookie (only send it in a first-party context).</td>
</tr>
<tr>
<td>d</td>
<td>Downgrade the cookie, if it is a persistent cookie, to a session cookie.</td>
</tr>
</table>
 

Logical rules are evaluated in the order they are listed. The first logical-rule to be matched, if any, determines the cookie action.

An empty expression is also allowed. If an expression is empty, the left side evaluates to true. This form of a logical-rule can be used at the end of a set of rules to catch all situations that did not fall into the other categories.

The following examples show valid logical rules. 


``` syntax
/DEM=d/
    Deny a cookie whose compact policy contains the DEM token
/CON&!TEL=a/	
    Accept a cookie whose compact policy contains the CON token 
    and does not contain the TEL token
/=a/		
    Accept all cookies
```

Special rules are specified using the nopolicy, session, and always symbols. The nopolicy symbol is used to specify the action to taken when there is no compact policy. For example nopolicy=d specifies to downgrade all cookies without a compact policy to session cookies. The session symbol is used to specify the action to take on session cookies and can only be set to a. When session=a is specified, all session cookies are accepted regardless of the content of the compact policy. If this rule is not specified, session cookies are subject to the same rules as persistent cookies. Finally, the always symbol is used to specify to perform the same action for everything. For example, always=d specifies to deny all cookies regardless of the existence of a compact policy. Note that always=d is equivalent to /=d/.

The following example shows a privacy preferences string that specifies to accept cookies for which the compact policy contains a FIN/CONi token pair, reject cookies with compact policies containing FIN/CON, FIN/CONo, FIN/CONa and GOV/PUB token pairs or a TEL token, and to prompt the user when a cookie's compact policy contains the UNR token. It also specifies to downgrade cookies without a compact policy to session cookies and to accept all cookies that do not match one of the given rules. Note that the first rule that evaluates to true determines the cookie action. 


``` syntax
IE6-P3PSettings/V1: /FIN&CONi=a/ /FIN&CONo=r/ /FIN&CONa=r/ /FIN&CON=r/ 
/GOV&PUB=r/ /TEL=r/ /UNR=p/ nopolicy=d /=a/
```

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetclearallpersitecookiedecisions">InternetClearAllPerSiteCookieDecisions</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetenumpersitecookiedecisiona">InternetEnumPerSiteCookieDecision</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetgetpersitecookiedecisiona">InternetGetPerSiteCookieDecision</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetpersitecookiedecisiona">InternetSetPerSiteCookieDecision</a>



<a href="/windows/desktop/api/wininet/nf-wininet-privacygetzonepreferencew">PrivacyGetZonePreferenceW</a>

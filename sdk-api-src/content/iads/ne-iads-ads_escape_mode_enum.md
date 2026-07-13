---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0078_0004
title: ADS_ESCAPE_MODE_ENUM (iads.h)
description: Specifies how escape characters are displayed in a directory path.
helpviewer_keywords: ["ADS_ESCAPEDMODE_DEFAULT","ADS_ESCAPEDMODE_OFF","ADS_ESCAPEDMODE_OFF_EX","ADS_ESCAPEDMODE_ON","ADS_ESCAPE_MODE_ENUM","ADS_ESCAPE_MODE_ENUM enumeration [ADSI]","_ds_ads_escape_mode_enum","adsi.ads__escape__mode__enum","adsi.ads_escape_mode_enum","iads/ADS_ESCAPEDMODE_DEFAULT","iads/ADS_ESCAPEDMODE_OFF","iads/ADS_ESCAPEDMODE_OFF_EX","iads/ADS_ESCAPEDMODE_ON","iads/ADS_ESCAPE_MODE_ENUM"]
old-location: adsi\ads_escape_mode_enum.htm
tech.root: adsi
ms.assetid: f69934bc-69ac-4822-b92d-89c94f55e036
ms.date: 12/05/2018
ms.keywords: ADS_ESCAPEDMODE_DEFAULT, ADS_ESCAPEDMODE_OFF, ADS_ESCAPEDMODE_OFF_EX, ADS_ESCAPEDMODE_ON, ADS_ESCAPE_MODE_ENUM, ADS_ESCAPE_MODE_ENUM enumeration [ADSI], _ds_ads_escape_mode_enum, adsi.ads__escape__mode__enum, adsi.ads_escape_mode_enum, iads/ADS_ESCAPEDMODE_DEFAULT, iads/ADS_ESCAPEDMODE_OFF, iads/ADS_ESCAPEDMODE_OFF_EX, iads/ADS_ESCAPEDMODE_ON, iads/ADS_ESCAPE_MODE_ENUM
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADS_ESCAPE_MODE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0078_0004
 - iads/__MIDL___MIDL_itf_ads_0001_0078_0004
 - ADS_ESCAPE_MODE_ENUM
 - iads/ADS_ESCAPE_MODE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_ESCAPE_MODE_ENUM
---

# ADS_ESCAPE_MODE_ENUM enumeration


## -description

The <b>ADS_ESCAPE_MODE_ENUM</b> enumeration specifies how escape characters are displayed in a directory path.

## -enum-fields

### -field ADS_ESCAPEDMODE_DEFAULT:1

The default escape mode provides a convenient option to specify the escape mode. It has the effect of minimal escape operation appropriate for a chosen format. Thus, the default behavior depends on the value that  <a href="/windows/win32/api/iads/ne-iads-ads_format_enum">ADS_FORMAT_ENUM</a> uses to retrieve the directory paths.

<table>
<tr>
<th>Retrieved path format</th>
<th>Default escaped mode</th>
</tr>
<tr>
<td><b>ADS_FORMAT_X500</b></td>
<td><b>ADS_ESCAPEDMODE_ON</b></td>
</tr>
<tr>
<td><b>ADS_FORMAT_X500_NO_SERVER</b></td>
<td><b>ADS_ESCAPEDMODE_ON</b></td>
</tr>
<tr>
<td><b>ADS_FORMAT_WINDOWS</b></td>
<td><b>ADS_ESCAPEDMODE_ON</b></td>
</tr>
<tr>
<td><b>ADS_FORMAT_WINDOWS_NO_SERVER</b></td>
<td><b>ADS_ESCAPEDMODE_ON</b></td>
</tr>
<tr>
<td><b>ADS_FORMAT_X500_DN</b></td>
<td><b>ADS_ESCAPEDMODE_OFF</b></td>
</tr>
<tr>
<td><b>ADS_FORMAT_X500_PARENT</b></td>
<td><b>ADS_ESCAPEDMODE_OFF</b></td>
</tr>
<tr>
<td><b>ADS_FORMAT_WINDOWS_DN</b></td>
<td><b>ADS_ESCAPEDMODE_OFF</b></td>
</tr>
<tr>
<td><b>ADS_FORMAT_WINDOWS_PARENT</b></td>
<td><b>ADS_ESCAPEDMODE_OFF</b></td>
</tr>
<tr>
<td><b>ADS_FORMAT_LEAF</b></td>
<td><b>ADS_ESCAPEDMODE_ON</b></td>
</tr>
</table>

### -field ADS_ESCAPEDMODE_ON:2

All special characters are displayed in the escape format; for example, "CN=date\=yy\/mm\/dd\,weekday" appears as is.

### -field ADS_ESCAPEDMODE_OFF:3

ADSI special characters are displayed in the unescaped format; for example, "CN=date\=yy\/mm\/dd\,weekday" appears as "CN=date\=yy/mm/dd\,weekday".

### -field ADS_ESCAPEDMODE_OFF_EX:4

ADSI and LDAP special characters are displayed in the  unescaped format; for example, "CN=date\=yy\/mm\/dd\,weekday" appears as "CN=date=yy/mm/dd,weekday".

## -remarks

Special characters must be escaped when used for any unintended purposes. For example, LDAP special characters, the comma (,) and the equal sign (=), are intended as field separators in a distinguished name, "CN=user,CN=users,DC=Fabrikam,DC=com". When an attribute value uses such special characters, for example, "CN=users\,last name\=Smith", these special characters must be escaped as shown. This ensures that an LDAP-compliant directory, such as Active Directory, will parse the path properly. However, an escaped path string may not appear to be user-friendly on a display. In this case, you can set the <b>ADS_ESCAPE_MODE_ENUM</b> in such way that shows the path as an unescaped string, "CN=users,last name=Smith".

Similarly, the ADSI special character, slash mark (/), separates ADSI-specific elements, "LDAP://server/CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=com". Although it must be escaped when used for any other purposes, for example, "LDAP://server/CN=Jeff Smith\/California,CN=Users,DC=Fabrikam,DC=com". You can choose an <b>ADS_ESCAPE_MODE_ENUM</b> option to display this escaped string in a human-readable form: "LDAP://server/CN=Jeff Smith/California,CN=Users,DC=Fabrikam,DC=com".

Presently, the slash mark (/) is the only ADSI special character. ADSI escaping and unescaping applies to ADSI special characters only. The operation will not affect any LDAP special characters, that is, they are neither escaped nor unescaped. For more information and  a list of  special characters defined by LDAP, see <a href="/windows/desktop/ADSI/ldap-adspath">LDAP Special Characters</a>.

To show unescaped path string, use 
the <a href="/windows/desktop/api/iads/nn-iads-iadspathname">IADsPathname</a> interface and its methods. All other ADSI APIs return the escaped path string.

To obtain correct behavior, the LDAP special characters must be escaped before the ADSI special characters are escaped. The <a href="/windows/desktop/api/iads/nn-iads-iadspathname">IADsPathname</a> interface will escape the characters in the correct sequence.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, Visual Basic Scripting Edition (VBScript) applications do not recognize symbolic, as constants defined above. Instead, use the numerical constants instead to set the appropriate flags in your VBScript applications. To use the symbolic constants, write explicit declarations of such constants, as done here.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI
  Enumerations</a>



<a href="/windows/win32/api/iads/ne-iads-ads_format_enum">ADS_FORMAT_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspathname">IADsPathname</a>



<a href="/windows/desktop/ADSI/ldap-adspath">LDAP ADsPath</a>

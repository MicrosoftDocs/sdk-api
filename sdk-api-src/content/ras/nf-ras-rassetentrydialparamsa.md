---
UID: NF:ras.RasSetEntryDialParamsA
title: RasSetEntryDialParamsA function (ras.h)
description: The RasSetEntryDialParams function changes the connection information saved by the last successful call to the RasDial or RasSetEntryDialParams function for a specified phone-book entry. (ANSI)
helpviewer_keywords: ["RasSetEntryDialParamsA", "dwCallbackId", "dwSize", "dwSubEntry", "ras/RasSetEntryDialParamsA", "szCallbackNumber", "szDomain", "szEntryName", "szPassword", "szPhoneNumber", "szUserName"]
old-location: rras\rassetentrydialparams.htm
tech.root: RRAS
ms.assetid: e1acd68e-796e-49a2-8c7d-c0fd1a9764ef
ms.date: 12/05/2018
ms.keywords: RasSetEntryDialParams, RasSetEntryDialParams function [RAS], RasSetEntryDialParamsA, RasSetEntryDialParamsW, _ras_rassetentrydialparams, dwCallbackId, dwSize, dwSubEntry, ras/RasSetEntryDialParams, ras/RasSetEntryDialParamsA, ras/RasSetEntryDialParamsW, rras.rassetentrydialparams, szCallbackNumber, szDomain, szEntryName, szPassword, szPhoneNumber, szUserName
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasSetEntryDialParamsW (Unicode) and RasSetEntryDialParamsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasSetEntryDialParamsA
 - ras/RasSetEntryDialParamsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasSetEntryDialParams
 - RasSetEntryDialParamsA
 - RasSetEntryDialParamsW
---

# RasSetEntryDialParamsA function


## -description

The 
<b>RasSetEntryDialParams</b> function changes the connection information saved by the last successful call to the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or 
<b>RasSetEntryDialParams</b> function for a specified phone-book entry.

## -parameters

### -param unnamedParam1 [in]

Pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box. 



						

<b>Windows Me/98/95:  </b>This parameter should always be <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.

### -param unnamedParam2 [in]

Pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> structure that specifies the connection parameters to be associated with the phone-book entry. 
<b>RasSetEntryDialParams</b> uses the structure's members as follows. 



<table>
<tr>
<th>Member</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="dwSize"></a><a id="dwsize"></a><a id="DWSIZE"></a><dl>
<dt><b>dwSize</b></dt>
</dl>
</td>
<td width="60%">
Must specify the size of (<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a>) to identify the version of the structure.

</td>
</tr>
<tr>
<td width="40%"><a id="szEntryName"></a><a id="szentryname"></a><a id="SZENTRYNAME"></a><dl>
<dt><b>szEntryName</b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string that identifies the phone-book entry to set parameters for.

</td>
</tr>
<tr>
<td width="40%"><a id="szPhoneNumber"></a><a id="szphonenumber"></a><a id="SZPHONENUMBER"></a><dl>
<dt><b>szPhoneNumber</b></dt>
</dl>
</td>
<td width="60%">
Not used. Set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="szCallbackNumber"></a><a id="szcallbacknumber"></a><a id="SZCALLBACKNUMBER"></a><dl>
<dt><b>szCallbackNumber</b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string that contains the callback phone number. If <b>szCallbackNumber</b> is an empty string ( "" ), the callback number is not changed.

</td>
</tr>
<tr>
<td width="40%"><a id="szUserName"></a><a id="szusername"></a><a id="SZUSERNAME"></a><dl>
<dt><b>szUserName</b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string that contains the logon name of the user associated with this entry. If <b>szUserName</b> is an empty string, the user name is not changed.

</td>
</tr>
<tr>
<td width="40%"><a id="szPassword"></a><a id="szpassword"></a><a id="SZPASSWORD"></a><dl>
<dt><b>szPassword</b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string that contains the password for the user specified by <b>szUserName</b>. If <b>szUserName</b> is an empty string, the password is not changed. If <b>szPassword</b> is an empty string and <i>fRemovePassword</i> is <b>FALSE</b>, the password is set to the empty string. If <i>fRemovePassword</i> is <b>TRUE</b>, the password stored in this phone-book entry for the user specified by <b>szUserName</b> is removed regardless of the contents of the <b>szPassword</b> string. 




<b>Windows NT 4.0:  </b>The password is changed to the string specified by <b>szPassword</b> regardless of whether <b>szUserName</b> is an empty string.

<b>Windows XP/2000:  </b>If <b>szPassword</b> contains the password handle returned by 
<a href="/windows/desktop/api/ras/nf-ras-rasgetcredentialsa">RasGetCredentials</a> or 
<a href="/windows/desktop/api/ras/nf-ras-rasgetentrydialparamsa">RasGetEntryDialParams</a>, 
<b>RasSetEntryDialParams</b> returns successfully without changing any currently saved password.

</td>
</tr>
<tr>
<td width="40%"><a id="szDomain"></a><a id="szdomain"></a><a id="SZDOMAIN"></a><dl>
<dt><b>szDomain</b></dt>
</dl>
</td>
<td width="60%">
A null-terminated string that contains the name of the domain on which to log on. If <b>szDomain</b> is an empty string, the domain name is not changed.

</td>
</tr>
<tr>
<td width="40%"><a id="dwSubEntry"></a><a id="dwsubentry"></a><a id="DWSUBENTRY"></a><dl>
<dt><b>dwSubEntry</b></dt>
</dl>
</td>
<td width="60%">
Specifies the (one-based) index of the initial subentry to dial when establishing the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="dwCallbackId"></a><a id="dwcallbackid"></a><a id="DWCALLBACKID"></a><dl>
<dt><b>dwCallbackId</b></dt>
</dl>
</td>
<td width="60%">
Specifies an application-defined value that RAS passes to the 
<a href="/windows/desktop/api/ras/nc-ras-rasdialfunc2">RasDialFunc2</a> callback function.

</td>
</tr>
</table>

### -param unnamedParam3 [in]

Specifies whether to remove the phone-book entry's stored password for the user indicated by <i>lprasdialparams</i>-&gt;<b>szUserName</b>. If <i>fRemovePassword</i> is <b>TRUE</b>, the password is removed. Setting fRemovePassword to <b>TRUE</b> is equivalent to checking the "Unsave Password" check box in Dial-Up Networking. When setting the password or other properties of a phone book entry, set <i>fRemovePassword</i> to <b>FALSE</b>.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The address or buffer specified by <i>lprasdialparams</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
The phone book is corrupted or missing components.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
The phone-book entry does not exist.

</td>
</tr>
</table>

## -remarks

To create a new phone-book entry, use the 
<a href="/windows/desktop/api/ras/nf-ras-rassetentrypropertiesa">RasSetEntryProperties</a> function.

<b>Windows XP or later:  </b>Do not use the 
<b>RasSetEntryDialParams</b> function. To set the credentials for a phone-book entry, use the 
<a href="/windows/desktop/api/ras/nf-ras-rassetcredentialsa">RasSetCredentials</a> function. Set the non-credential members of 
<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a> (for example <b>szCallbackNumber</b>, <b>dwSubEntry</b>, or <b>dwCallbackId</b>) directly in the 
<b>RASDIALPARAMS</b> structure passed as a parameter to the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function.





> [!NOTE]
> The ras.h header defines RasSetEntryDialParams as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)">RASDIALPARAMS</a>



<a href="/windows/desktop/api/ras/nf-ras-rascreatephonebookentrya">RasCreatePhonebookEntry</a>



<a href="/windows/desktop/api/ras/nf-ras-raseditphonebookentrya">RasEditPhonebookEntry</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetentrydialparamsa">RasGetEntryDialParams</a>



<a href="/windows/desktop/api/ras/nf-ras-rassetcredentialsa">RasSetCredentials</a>



<a href="/windows/desktop/api/ras/nf-ras-rassetentrypropertiesa">RasSetEntryProperties</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>

---
UID: NF:ras.RasSetAutodialAddressA
title: RasSetAutodialAddressA function (ras.h)
description: The RasSetAutodialAddress function can add an address to the AutoDial mapping database. Alternatively, the function can delete or modify the data associated with an existing address in the database. (ANSI)
helpviewer_keywords: ["RasSetAutodialAddressA", "ras/RasSetAutodialAddressA"]
old-location: rras\rassetautodialaddress.htm
tech.root: RRAS
ms.assetid: 267d4f8e-0e0b-4636-8f30-3c39bbb8d4e9
ms.date: 12/05/2018
ms.keywords: RasSetAutodialAddress, RasSetAutodialAddress function [RAS], RasSetAutodialAddressA, RasSetAutodialAddressW, _ras_rassetautodialaddress, ras/RasSetAutodialAddress, ras/RasSetAutodialAddressA, ras/RasSetAutodialAddressW, rras.rassetautodialaddress
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasSetAutodialAddressW (Unicode) and RasSetAutodialAddressA (ANSI)
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
 - RasSetAutodialAddressA
 - ras/RasSetAutodialAddressA
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
 - RasSetAutodialAddress
 - RasSetAutodialAddressA
 - RasSetAutodialAddressW
---

# RasSetAutodialAddressA function


## -description

The 
<b>RasSetAutodialAddress</b> function can add an address to the AutoDial mapping database. Alternatively, the function can delete or modify the data associated with an existing address in the database.

## -parameters

### -param unnamedParam1 [in]

Pointer to a <b>null</b>-terminated string that specifies the address to add, delete, or modify. This address can be an IP address, Internet host name ("www.microsoft.com"), or NetBIOS name ("products1"). 




If this parameter is <b>NULL</b>, the function sets the default Internet connection (see Remarks). If this parameter points to a zero-length string, the function deletes the default Internet connection.

### -param unnamedParam2 [in]

Reserved; must be zero.

### -param unnamedParam3 [in]

Pointer to an array of one or more 
<a href="/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)">RASAUTODIALENTRY</a> structures to be associated with the <i>lpszAddress</i> address. If <i>lpAutoDialEntries</i> is <b>NULL</b> and <i>dwcbAutoDialEntries</i> is zero, 
<b>RasSetAutodialAddress</b> deletes all structures associated with <i>lpszAddress</i> from the mapping database.

### -param unnamedParam4 [in]

Specifies the size, in bytes, of the <i>lpAutoDialEntries</i> buffer.

### -param unnamedParam5 [in]

Specifies the number of 
<a href="/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)">RASAUTODIALENTRY</a> structures in the <i>lpAutoDialEntries</i> buffer.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwSize</b> member of the 
<a href="/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)">RASAUTODIALENTRY</a> structure is an invalid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpszAddress</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
The connection name specified in <i>lpAutoDialEntries</i> does not exist.

</td>
</tr>
</table>

## -remarks

An address in the AutoDial mapping database can have any number of associated 
<a href="/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)">RASAUTODIALENTRY</a> entries. Each entry specifies AutoDial information for a particular TAPI dialing location.

If the address specified by the <i>lpszAddress</i> parameter is an existing address in the database and the <i>lpAutoDialEntries</i> parameter is not <b>NULL</b>, the 
<b>RasSetAutodialAddress</b> function modifies the set of AutoDial entries associated with the address. If an entry in the <i>lpAutoDialEntries</i> array specifies a dialing location for which the address already has an entry, the function replaces the existing entry with the new entry. Otherwise, the function simply adds the <i>lpAutoDialEntries</i> entries to the set of entries for the address.

If the <i>lpszAddress</i> address exists in the database, <i>lpAutoDialEntries</i> is <b>NULL</b>, and <i>lpAutoDialEntries</i> is zero, 
<b>RasSetAutodialAddress</b> deletes the address from the database.

If the <i>lpszAddress</i> address does not exist in the database, 
<b>RasSetAutodialAddress</b> adds the address to the database. The <i>lpAutoDialEntries</i> parameter specifies the AutoDial entries to associate with the new address.

 RAS supports a default Internet connection that is global to the local computer and  supports a default Internet connection for each user.

When the <i>lpszAddress</i> parameter is <b>NULL</b>, and the <i>lpAutoDialEntries</i> parameter specifies a connection name with one entry, <b>RasSetAutodialAddress</b> sets the connection as the default internet connection.  The connection name specified in  <i>lpAutoDialEntries</i> should already exist.  If it does not, <b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b> will be returned.

When the <i>lpszAddress</i> parameter is a zero-length string and the <i>lpAutoDialEntries</i> parameter specifies an empty connection name with one entry, <b>RasSetAutodialAddress</b> deletes the default internet connection.

On non-domain client machines, if a user wants to set a connection as the default internet connection and specifies a "for-all-users" connection in the <b>szEntry</b> member of the <a href="/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)">RASAUTODIALENTRY</a> structure, then the default internet connection is set globally on the local computer.  In all other cases the default internet connection is set for each user of the machine individually.

It is possible to have two connections that have the same name if one is configured as a "for-all-users" connection and the other is configured as a "for-me-only" connection. If the <i>lpAutoDialEntries</i> parameter specifies a connection name that corresponds to both a global and a per-user connection, the per-user connection is set.





> [!NOTE]
> The ras.h header defines RasSetAutodialAddress as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)">RASAUTODIALENTRY</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumautodialaddressesa">RasEnumAutodialAddresses</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetautodialaddressa">RasGetAutodialAddress</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>

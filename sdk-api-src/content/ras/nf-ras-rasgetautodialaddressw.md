---
UID: NF:ras.RasGetAutodialAddressW
title: RasGetAutodialAddressW function (ras.h)
description: The RasGetAutodialAddress function retrieves information about all the AutoDial entries associated with a network address in the AutoDial mapping database. (Unicode)
helpviewer_keywords: ["RasGetAutodialAddress", "RasGetAutodialAddress function [RAS]", "RasGetAutodialAddressW", "_ras_rasgetautodialaddress", "ras/RasGetAutodialAddress", "ras/RasGetAutodialAddressW", "rras.rasgetautodialaddress"]
old-location: rras\rasgetautodialaddress.htm
tech.root: RRAS
ms.assetid: b7182760-30c0-4c09-ae99-f656d868e150
ms.date: 12/05/2018
ms.keywords: RasGetAutodialAddress, RasGetAutodialAddress function [RAS], RasGetAutodialAddressA, RasGetAutodialAddressW, _ras_rasgetautodialaddress, ras/RasGetAutodialAddress, ras/RasGetAutodialAddressA, ras/RasGetAutodialAddressW, rras.rasgetautodialaddress
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetAutodialAddressW (Unicode) and RasGetAutodialAddressA (ANSI)
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
 - RasGetAutodialAddressW
 - ras/RasGetAutodialAddressW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-rasapi32-l1-1-2.dll
 - Rasapi32.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasGetAutodialAddress
 - RasGetAutodialAddressA
 - RasGetAutodialAddressW
---

# RasGetAutodialAddressW function


## -description

The 
<b>RasGetAutodialAddress</b> function retrieves information about all the AutoDial entries associated with a network address in the AutoDial mapping database.

## -parameters

### -param unnamedParam1 [in]

Pointer to a <b>null</b>-terminated string that specifies the address for which information is requested. This can be an IP address, Internet host name ("www.microsoft.com"), or NetBIOS name ("products1").

If this parameter is <b>NULL</b>, the function retrieves the default Internet connection. The function returns the per-user default Internet connection if one is configured. Otherwise, the function returns the global default Internet connection. If no default Internet connections are configured, the function returns zero for the <i>lpdwcbAutoDialEntries</i> and <i>lpdwcAutoDialEntries</i> parameters.

### -param unnamedParam2 [in]

Reserved; must be <b>NULL</b>.

### -param unnamedParam3 [in, out]

Pointer to a buffer that, on output, receives an array of 
<a href="/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)">RASAUTODIALENTRY</a> structures, one for each AutoDial entry associated with the address specified by the <i>lpszAddress</i> parameter. 




On input, set the <b>dwSize</b> member of the first 
<a href="/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)">RASAUTODIALENTRY</a> structure in the buffer to sizeof(RASAUTODIALENTRY) to identify the version of the structure.

If <i>lpAutoDialEntries</i> is <b>NULL</b>, 
<b>RasGetAutodialAddress</b> sets the <i>lpdwcbAutoDialEntries</i> and <i>lpdwcAutoDialEntries</i> parameters to indicate the required buffer size, in bytes, and the number of AutoDial entries.

### -param unnamedParam4 [in, out]

Pointer to a variable that, on input, specifies the size, in bytes, of the <i>lpAutoDialEntries</i> buffer. 




On output, this variable receives the number of bytes returned, or the number of bytes required if the buffer is too small.

### -param unnamedParam5 [out]

Pointer to a variable that receives the number of structure elements returned in the <i>lpAutoDialEntries</i> buffer.

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
The <i>lpszAddress</i>, <i>lpdwcbAutoDialEntries</i>, or <i>lpdwcAutoDialEntries</i> parameter was <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The Remote Access Service (RAS) supports default Internet connections. RAS supports a default Internet connection that is global to the local computer, and in addition, supports a default Internet connection for each user.

The name of the global default Internet connection is stored in the registry below the following registry key:


<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Ras Autodial</b>
            <b>Default</b></pre>


The value that stores the name of the connection is: 
			

<b>DefaultInternet</b>

This value is of type <b>REG_SZ</b>.

The global default Internet connection must be configured as a <b>For all users</b> connection in the <b>Connections Folder</b> user interface.

The name of the per-user default Internet connection is stored in the registry below the following registry key: 
			


<b>HKEY_CURRENT_USER</b>&#92;<b>Software</b>&#92;<b>Microsoft</b>&#92;<b>Ras Autodial</b>&#92;<b>Default</b>



The value that stores the name of the connection is: 
			

<b>DefaultInternet</b>

This value is of type <b>REG_SZ</b>.





> [!NOTE]
> The ras.h header defines RasGetAutodialAddress as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)">RASAUTODIALENTRY</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumautodialaddressesa">RasEnumAutodialAddresses</a>



<a href="/windows/desktop/api/ras/nf-ras-rassetautodialaddressa">RasSetAutodialAddress</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>

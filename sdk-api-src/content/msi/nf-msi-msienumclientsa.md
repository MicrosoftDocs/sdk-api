---
UID: NF:msi.MsiEnumClientsA
title: MsiEnumClientsA function (msi.h)
description: The MsiEnumClients function enumerates the clients for a given installed component. The function retrieves one product code each time it is called. (ANSI)
helpviewer_keywords: ["MsiEnumClientsA", "msi/MsiEnumClientsA"]
old-location: setup\msienumclients.htm
tech.root: setup
ms.assetid: 681c1c77-e3b2-4bb5-81f6-4eeadafcc404
ms.date: 12/05/2018
ms.keywords: MsiEnumClients, MsiEnumClients function, MsiEnumClientsA, MsiEnumClientsW, _msi_msienumclients, msi/MsiEnumClients, msi/MsiEnumClientsA, msi/MsiEnumClientsW, setup.msienumclients
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiEnumClientsW (Unicode) and MsiEnumClientsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiEnumClientsA
 - msi/MsiEnumClientsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiEnumClients
 - MsiEnumClientsA
 - MsiEnumClientsW
---

# MsiEnumClientsA function


## -description

The 
<b>MsiEnumClients</b> function enumerates the clients for a given installed component. The function retrieves one product code each time it is called.

## -parameters

### -param szComponent [in]

Specifies the component whose clients are to be enumerated.

### -param iProductIndex [in]

Specifies the index of the client to retrieve. This parameter should be zero for the first call to the 
<b>MsiEnumClients</b> function and then incremented for subsequent calls. Because clients are not ordered, any new client has an arbitrary index. This means that the function can return clients in any order.

### -param lpProductBuf [out]

Pointer to a buffer that receives the product code. This buffer must be 39 characters long. The first 38 characters are for the GUID, and the last character is for the terminating null character.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no clients to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system does not have enough memory to complete the operation. Available with Windows Server 2003.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
A value was enumerated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_COMPONENT</b></dt>
</dl>
</td>
<td width="60%">
The specified component is unknown.

</td>
</tr>
</table>

## -remarks

To enumerate clients, an application should initially call the 
<b>MsiEnumClients</b> function with the<i> iProductIndex</i> parameter set to zero. The application should then increment the <i> iProductIndex</i> parameter and call 
<b>MsiEnumClients</b> until there are no more clients (that is, until the function returns ERROR_NO_MORE_ITEMS).

When making multiple calls to 
<b>MsiEnumClients</b> to enumerate all of the component's clients, each call should be made from the same thread.





> [!NOTE]
> The msi.h header defines MsiEnumClients as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>

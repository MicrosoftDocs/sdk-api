---
UID: NF:msi.MsiNotifySidChangeW
title: MsiNotifySidChangeW function (msi.h)
description: The MsiNotifySidChange function notifies and updates the Windows Installer internal information with changes to user SIDs. (Unicode)
helpviewer_keywords: ["MsiNotifySidChange", "MsiNotifySidChange function", "MsiNotifySidChangeW", "msi/MsiNotifySidChange", "msi/MsiNotifySidChangeW", "setup.msinotifysidchange"]
old-location: setup\msinotifysidchange.htm
tech.root: setup
ms.assetid: f35e503e-0bc0-4895-8e88-fc5636774e75
ms.date: 12/05/2018
ms.keywords: MsiNotifySidChange, MsiNotifySidChange function, MsiNotifySidChangeA, MsiNotifySidChangeW, msi/MsiNotifySidChange, msi/MsiNotifySidChangeA, msi/MsiNotifySidChangeW, setup.msinotifysidchange
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.1 on Windows Server 2003, Windows XP, and Windows 2000. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiNotifySidChangeW (Unicode) and MsiNotifySidChangeA (ANSI)
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
 - MsiNotifySidChangeW
 - msi/MsiNotifySidChangeW
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
 - MsiNotifySidChange
 - MsiNotifySidChangeA
 - MsiNotifySidChangeW
---

# MsiNotifySidChangeW function


## -description

The <b>MsiNotifySidChange</b> function notifies and updates the Windows Installer internal information  with changes to  user SIDs.

## -parameters

### -param pOldSid [in]

Null-terminated string that specifies the string value of the previous security identifier(SID).

### -param pNewSid [in]

Null-terminated string that specifies the string value of the new security identifier(SID).

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter is passed to the function. This error returned if any of the parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory was available.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Internal failure during execution.


</td>
</tr>
</table>

## -remarks

<b>Windows Installer 2.0 and Windows Installer 3.0:  </b>Not supported. This function is available beginning with Windows Installer 3.1.





> [!NOTE]
> The msi.h header defines MsiNotifySidChange as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-3-0">Not Supported in Windows Installer 3.0 and earlier</a>

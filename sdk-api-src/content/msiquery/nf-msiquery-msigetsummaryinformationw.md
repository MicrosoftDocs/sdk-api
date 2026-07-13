---
UID: NF:msiquery.MsiGetSummaryInformationW
title: MsiGetSummaryInformationW function (msiquery.h)
description: The MsiGetSummaryInformation function obtains a handle to the _SummaryInformation stream for an installer database. This function returns a handle that should be closed using MsiCloseHandle. (Unicode)
helpviewer_keywords: ["MsiGetSummaryInformation", "MsiGetSummaryInformation function", "MsiGetSummaryInformationW", "_msi_msigetsummaryinformation", "msiquery/MsiGetSummaryInformation", "msiquery/MsiGetSummaryInformationW", "setup.msigetsummaryinformation"]
old-location: setup\msigetsummaryinformation.htm
tech.root: setup
ms.assetid: f3a6d7cc-83b2-45c6-bf86-c579b39c2c92
ms.date: 12/05/2018
ms.keywords: MsiGetSummaryInformation, MsiGetSummaryInformation function, MsiGetSummaryInformationA, MsiGetSummaryInformationW, _msi_msigetsummaryinformation, msiquery/MsiGetSummaryInformation, msiquery/MsiGetSummaryInformationA, msiquery/MsiGetSummaryInformationW, setup.msigetsummaryinformation
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetSummaryInformationW (Unicode) and MsiGetSummaryInformationA (ANSI)
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
 - MsiGetSummaryInformationW
 - msiquery/MsiGetSummaryInformationW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
 - MsiGetSummaryInformation
 - MsiGetSummaryInformationA
 - MsiGetSummaryInformationW
---

# MsiGetSummaryInformationW function


## -description

The 
<b>MsiGetSummaryInformation</b> function obtains a handle to the _SummaryInformation stream for an installer database. This function returns a handle that should be closed using 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>.

## -parameters

### -param hDatabase [in]

Handle to the database.

### -param szDatabasePath [in]

Specifies the path to the database.

### -param uiUpdateCount [in]

Specifies the maximum number of updated values.

### -param phSummaryInfo [out]

Pointer to the location from which to receive the summary information handle.

## -returns

The 
<b>MsiGetSummaryInformation</b> function returns the following values:

## -remarks

If the database specified by the 
<b>MsiGetSummaryInformation</b> function is not open, you must specify 0 for <i>hDatabase</i> and specify the path to the database in <i>szDatabasePath</i>. If the database is open, you must set <i>szDatabasePath</i> to 0.

If a value of <i>uiUpdateCount</i> greater than 0 is used to open an existing summary information stream, 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msisummaryinfopersist">MsiSummaryInfoPersist</a> must be called before closing the <i>phSummaryInfo</i> handle. Failing to do this will lose the existing stream information.

To view the summary information of a patch using <b>MsiGetSummaryInformation</b>, set <i>szDatabasePath</i> to the path to the patch. Alternately, you can create a handle to the patch using 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiopendatabasea">MsiOpenDatabase</a> and then pass that handle to 
<b>MsiGetSummaryInformation</b> as the <i>hDatabase</i> parameter.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>. For more information see <a href="/windows/desktop/Msi/windows-installer-best-practices">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="/windows/desktop/Msi/windows-installer-best-practices">Windows Installer Best Practices</a>.

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.





> [!NOTE]
> The msiquery.h header defines MsiGetSummaryInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Summary Information Property Functions</a>



<a href="/windows/desktop/Msi/summary-information-stream-property-set">Summary Information Stream Property Set</a>

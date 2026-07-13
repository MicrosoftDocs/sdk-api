---
UID: NF:msiquery.MsiGetLastErrorRecord
title: MsiGetLastErrorRecord function (msiquery.h)
description: The MsiGetLastErrorRecord function returns the error record that was last returned for the calling process. This function returns a handle that should be closed using MsiCloseHandle.
helpviewer_keywords: ["MsiGetLastErrorRecord","MsiGetLastErrorRecord function","_msi_msigetlasterrorrecord","msiquery/MsiGetLastErrorRecord","setup.msigetlasterrorrecord"]
old-location: setup\msigetlasterrorrecord.htm
tech.root: setup
ms.assetid: 0d6f4506-367b-43d7-ba1c-2a93c1d0cc51
ms.date: 12/05/2018
ms.keywords: MsiGetLastErrorRecord, MsiGetLastErrorRecord function, _msi_msigetlasterrorrecord, msiquery/MsiGetLastErrorRecord, setup.msigetlasterrorrecord
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - MsiGetLastErrorRecord
 - msiquery/MsiGetLastErrorRecord
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
 - MsiGetLastErrorRecord
---

# MsiGetLastErrorRecord function


## -description

The 
<b>MsiGetLastErrorRecord</b> function returns the error record that was last returned for the calling process. This function returns a handle that should be closed using 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>.



## -returns

A handle to the error record. If the last function was successful, 
<b>MsiGetLastErrorRecord</b> returns a null <b>MSIHANDLE</b>.

## -remarks

With the 
<b>MsiGetLastErrorRecord</b> function, field 1 of the record contains the installer error code. Other fields contain data specific to the particular error. The error record is released internally after this function is run.

If the record is passed to 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiprocessmessage">MsiProcessMessage</a>, it is formatted by looking up the string in the current database. If there is no installation session but a product database is open, the format string may be obtained by a query on the 
<a href="/windows/desktop/Msi/error-table">Error table</a> using the error code, followed by a call to 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiformatrecorda">MsiFormatRecord</a>. If the error code is known, the parameters may be individually interpreted.

The following functions set the per-process error record or reset it to null if no error occurred. <b>MsiGetLastErrorRecord</b> also clears the error record after returning it.

<ul>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiopendatabasea">MsiOpenDatabase</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabasecommit">MsiDatabaseCommit</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabaseopenviewa">MsiDatabaseOpenView</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabaseimporta">MsiDatabaseImport</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabaseexporta">MsiDatabaseExport</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabasemergea">MsiDatabaseMerge</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabasegeneratetransforma">MsiDatabaseGenerateTransform</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabaseapplytransforma">MsiDatabaseApplyTransform</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewexecute">MsiViewExecute</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewmodify">MsiViewModify</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msirecordsetstreama">MsiRecordSetStream</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetsummaryinformationa">MsiGetSummaryInformation</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetsourcepatha">MsiGetSourcePath</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigettargetpatha">MsiGetTargetPath</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msisettargetpatha">MsiSetTargetPath</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetcomponentstatea">MsiGetComponentState</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msisetcomponentstatea">MsiSetComponentState</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetfeaturestatea">MsiGetFeatureState</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msisetfeaturestatea">MsiSetFeatureState</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetfeaturecosta">MsiGetFeatureCost</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetfeaturevalidstatesa">MsiGetFeatureValidStates</a>
</li>
<li>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msisetinstalllevel">MsiSetInstallLevel</a>
</li>
</ul>
Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>. For more information see <a href="/windows/desktop/Msi/windows-installer-best-practices">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="/windows/desktop/Msi/windows-installer-best-practices">Windows Installer Best Practices</a>.

The following sample uses a call to <a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabaseopenviewa">MsiDatabaseOpenView</a> to  show how to obtain extended error information from one of the Windows Installer functions that supports <b>MsiGetLastErrorRecord</b>.  The example, OpenViewOnDatabase,  attempts to open a view on a database                 handle. The <i>hDatabase</i> handle can be
obtained by a call to <a href="/windows/desktop/api/msiquery/nf-msiquery-msiopendatabasea">MsiOpenDatabase</a>. If opening
the view fails, the function then tries to obtain extended
error information by using <b>MsiGetLastErrorRecord</b>.



```cpp
#include <windows.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")
//-------------------------------------------------------------------
// Function: OpenViewOnDatabase
//
// Arguments: hDatabase - handle to a MSI package obtained
//                                        via a call to MsiOpenDatabase
//
// Returns: UINT status code. ERROR_SUCCESS for success.
//--------------------------------------------------------------------------------------------------
UINT __stdcall OpenViewOnDatabase(MSIHANDLE hDatabase)
{
    if (!hDatabase)
        return ERROR_INVALID_PARAMETER;

    PMSIHANDLE hView = 0;
    UINT uiReturn = MsiDatabaseOpenView(hDatabase, 
                                TEXT("SELECT * FROM `UnknownTable`"),
                           &hView);

    if (ERROR_SUCCESS != uiReturn)
    {
        // try to obtain extended error information.

        PMSIHANDLE hLastErrorRec = MsiGetLastErrorRecord();

        TCHAR* szExtendedError = NULL;
        DWORD cchExtendedError = 0;
        if (hLastErrorRec)
        {
            // Since we are not currently calling MsiFormatRecord during an
            // install session, hInstall is NULL. If MsiFormatRecord was called
            // via a DLL custom action, the hInstall handle provided to the DLL
            // custom action entry point could be used to further resolve 
            // properties that might be contained within the error record.
            
            // To determine the size of the buffer required for the text,
            // szResultBuf must be provided as an empty string with
            // *pcchResultBuf set to 0.

            UINT uiStatus = MsiFormatRecord(NULL,
                             hLastErrorRec,
                             TEXT(""),
                             &cchExtendedError);

            if (ERROR_MORE_DATA == uiStatus)
            {
                // returned size does not include null terminator.
                cchExtendedError++;

                szExtendedError = new TCHAR[cchExtendedError];
                if (szExtendedError)
                {
                    uiStatus = MsiFormatRecord(NULL,
                                     hLastErrorRec,
                                     szExtendedError,
                                     &cchExtendedError);
                    if (ERROR_SUCCESS == uiStatus)
                    {
                        // We now have an extended error
                        // message to report.

                        // PLACE ADDITIONAL CODE HERE
                        // TO LOG THE ERROR MESSAGE
                        // IN szExtendedError.
                    }

                    delete [] szExtendedError;
                    szExtendedError = NULL;
                }
            }
        }
    }

    return uiReturn;
}

```

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer State Access Functions</a>

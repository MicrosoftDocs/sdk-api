---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# MsiGetLastErrorRecord function


## -description


The 
<b>MsiGetLastErrorRecord</b> function returns the error record that was last returned for the calling process. This function returns a handle that should be closed using 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>.


## -parameters






## -returns



A handle to the error record. If the last function was successful, 
<b>MsiGetLastErrorRecord</b> returns a null <b>MSIHANDLE</b>.




## -remarks



With the 
<b>MsiGetLastErrorRecord</b> function, field 1 of the record contains the installer error code. Other fields contain data specific to the particular error. The error record is released internally after this function is run.

If the record is passed to 
<a href="https://msdn.microsoft.com/136662bd-b970-4ff3-8ae5-c5e3097ee00d">MsiProcessMessage</a>, it is formatted by looking up the string in the current database. If there is no installation session but a product database is open, the format string may be obtained by a query on the 
<a href="https://msdn.microsoft.com/3c817468-cba7-46bf-9208-5e6699c02fb6">Error table</a> using the error code, followed by a call to 
<a href="https://msdn.microsoft.com/574f51b1-a5cf-46c8-bfa3-449839872cf3">MsiFormatRecord</a>. If the error code is known, the parameters may be individually interpreted.

The following functions set the per-process error record or reset it to null if no error occurred. <b>MsiGetLastErrorRecord</b> also clears the error record after returning it.

<ul>
<li>
<a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bc42b90b-51db-4e13-af2f-4942923badf6">MsiDatabaseCommit</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1ef23f9a-7d79-4d07-9349-8e9c132f1b94">MsiDatabaseOpenView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/df277641-393e-4202-bb92-4b813ddaa0ca">MsiDatabaseImport</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c20c168d-900e-496a-894c-5678f308cdbe">MsiDatabaseExport</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2a8c5e13-f7af-47ea-b781-a739d848fe09">MsiDatabaseMerge</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9e8fc756-4195-4fb7-9adb-0bda20e4ae95">MsiDatabaseGenerateTransform</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a0222465-f778-43c1-8007-22df6a01f8bd">MsiDatabaseApplyTransform</a>
</li>
<li>
<a href="https://msdn.microsoft.com/12b2373f-425a-4035-bdb4-be1a5469f1d7">MsiViewExecute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/312c3e62-4c08-447b-951f-d8d944daff3e">MsiViewModify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ca62f6a6-2f39-4b4c-876f-4c74ecd28ee2">MsiRecordSetStream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f3a6d7cc-83b2-45c6-bf86-c579b39c2c92">MsiGetSummaryInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3cb8c3fa-6f0a-4829-befd-450e58c86962">MsiGetSourcePath</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cad0e1c1-3f3a-4438-8b85-ea146c943579">MsiGetTargetPath</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bfd39656-4901-442f-940d-424d440caf70">MsiSetTargetPath</a>
</li>
<li>
<a href="https://msdn.microsoft.com/343f5cbc-e026-4a51-9c54-da5d10b7caa8">MsiGetComponentState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d538c81f-130b-4522-9f85-47f04e24f125">MsiSetComponentState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb8942b9-996e-45d8-b515-5c84737eb5ed">MsiGetFeatureState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c7b22484-5a89-44f2-b0ff-6061a7fc5703">MsiSetFeatureState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/492968a5-d781-45de-a4b2-eb1be3f3f148">MsiGetFeatureCost</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c4c3f484-6854-4019-9dc0-e4c99162c339">MsiGetFeatureValidStates</a>
</li>
<li>
<a href="https://msdn.microsoft.com/98f1d91d-632e-4dea-948f-2dc416b4d410">MsiSetInstallLevel</a>
</li>
</ul>
Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>. For more information see <a href="windows_installer_best_practices.htm">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="https://msdn.microsoft.com/ff48d995-fe6f-4d1b-898d-67574ed3c5b7">Windows Installer Best Practices</a>.

The following sample uses a call to <a href="https://msdn.microsoft.com/1ef23f9a-7d79-4d07-9349-8e9c132f1b94">MsiDatabaseOpenView</a> to  show how to obtain extended error information from one of the Windows Installer functions that supports <b>MsiGetLastErrorRecord</b>.  The example, OpenViewOnDatabase,  attempts to open a view on a database                 handle. The <i>hDatabase</i> handle can be
obtained by a call to <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a>. If opening
the view fails, the function then tries to obtain extended
error information by using <b>MsiGetLastErrorRecord</b>.


<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;Msiquery.h&gt;
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
                           &amp;hView);

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
                             &amp;cchExtendedError);

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
                                     &amp;cchExtendedError);
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="database_functions.htm">Installer State Access Functions</a>
 

 


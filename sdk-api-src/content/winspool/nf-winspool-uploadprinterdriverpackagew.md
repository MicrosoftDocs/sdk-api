---
UID: NF:winspool.UploadPrinterDriverPackageW
title: UploadPrinterDriverPackageW function
author: windows-driver-content
description: Uploads a printer driver to the print server's driver store so that it can be installed by calling InstallPrinterDriverFromPackage.
old-location: gdi\uploadprinterdriverpackage.htm
old-project: printdocs
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: UPDP_CHECK_DRIVERSTORE, UPDP_SILENT_UPLOAD, UPDP_UPLOAD_ALWAYS, UploadPrinterDriverPackage, UploadPrinterDriverPackage function [Windows GDI], UploadPrinterDriverPackageA, UploadPrinterDriverPackageW, _win32_UploadPrinterDriverPackage, gdi.uploadprinterdriverpackage, winspool/UploadPrinterDriverPackage, winspool/UploadPrinterDriverPackageA, winspool/UploadPrinterDriverPackageW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UploadPrinterDriverPackageW (Unicode) and UploadPrinterDriverPackageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINT_EXECUTION_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Spoolss.dll
api_name:
-	UploadPrinterDriverPackage
-	UploadPrinterDriverPackageA
-	UploadPrinterDriverPackageW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Spoolss.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# UploadPrinterDriverPackageW function


## -description


Uploads a printer driver to the print server's driver store so that it can be installed by calling <a href="https://msdn.microsoft.com/5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0">InstallPrinterDriverFromPackage</a>.


## -parameters




### -param pszServer [in]

A pointer to a constant, null-terminated string that specifies the name of the print server. Use <b>NULL</b> if the server is the local computer.


### -param pszInfPath [in]

A pointer to a constant ,null-terminated string that specifies the source path to the driver's .inf file.


### -param pszEnvironment [in]

A pointer to a constant, null-terminated string that specifies the server's processor architecture (for example, Windows NT x86). This can be <b>NULL</b>.


### -param dwFlags [in]

This can be any of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UPDP_SILENT_UPLOAD"></a><a id="updp_silent_upload"></a><dl>
<dt><b>UPDP_SILENT_UPLOAD</b></dt>
</dl>
</td>
<td width="60%">
The UI will not be shown during the upload.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDP_UPLOAD_ALWAYS"></a><a id="updp_upload_always"></a><dl>
<dt><b>UPDP_UPLOAD_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
The files will be uploaded even if the package is already in the server's driver store.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDP_CHECK_DRIVERSTORE"></a><a id="updp_check_driverstore"></a><dl>
<dt><b>UPDP_CHECK_DRIVERSTORE</b></dt>
</dl>
</td>
<td width="60%">
The server's driver store will be checked before upload to see if the package is already there. This setting is ignored if UPDP_UPLOAD_ALWAYS is set.

</td>
</tr>
</table>
 


### -param hwnd [in]

A handle to the copying user interface.


### -param pszDestInfPath [out]

A pointer to the destination path, in the driver store, to which the driver's .inf file was copied.


### -param pcchDestInfPath [in, out]

On input, specifies the size, in characters, of the <i>pszDestInfPath</i> buffer. On output, receives the size, in characters, of the path string, including the terminating null character.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> will contain an error code.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
The driver store is typically either %windir%\inf or %windir%\System32\DriverStore\FileRepository.

Only one package at a time can be uploaded. If a package is dependent on others, they must be uploaded separately.

Only signed driver packages can be uploaded.




## -see-also




<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 


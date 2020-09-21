---
UID: NF:comadmin.ICOMAdminCatalog.InstallApplication
title: ICOMAdminCatalog::InstallApplication (comadmin.h)
description: Installs a COM+ application or application proxy from the specified file.
helpviewer_keywords: ["COMAdminInstallForceOverwriteOfFiles","COMAdminInstallNoUsers","COMAdminInstallUsers","ICOMAdminCatalog interface [COM+]","InstallApplication method","ICOMAdminCatalog.InstallApplication","ICOMAdminCatalog::InstallApplication","InstallApplication","InstallApplication method [COM+]","InstallApplication method [COM+]","ICOMAdminCatalog interface","_cos_ICOMAdminCatalog_InstallApplication","comadmin/ICOMAdminCatalog::InstallApplication","cos.icomadmincatalog_installapplication"]
old-location: cos\icomadmincatalog_installapplication.htm
tech.root: cos
ms.assetid: 668f73e1-7238-42f5-b68c-a0b0c2595d18
ms.date: 12/05/2018
ms.keywords: COMAdminInstallForceOverwriteOfFiles, COMAdminInstallNoUsers, COMAdminInstallUsers, ICOMAdminCatalog interface [COM+],InstallApplication method, ICOMAdminCatalog.InstallApplication, ICOMAdminCatalog::InstallApplication, InstallApplication, InstallApplication method [COM+], InstallApplication method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_InstallApplication, comadmin/ICOMAdminCatalog::InstallApplication, cos.icomadmincatalog_installapplication
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICOMAdminCatalog::InstallApplication
 - comadmin/ICOMAdminCatalog::InstallApplication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.InstallApplication
---

# ICOMAdminCatalog::InstallApplication


## -description

Installs a COM+ application or application proxy from the specified file.

## -parameters

### -param bstrApplicationFile [in]

The name of the file containing the application to be installed.

### -param bstrDestinationDirectory [in, optional]

Where to install the components. If this parameter is blank, the default directory is used.

### -param lOptions [in, optional]

The option flags. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COMAdminInstallNoUsers"></a><a id="comadmininstallnousers"></a><a id="COMADMININSTALLNOUSERS"></a><dl>
<dt><b>COMAdminInstallNoUsers</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Do not install users saved in application file (default).

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminInstallUsers"></a><a id="comadmininstallusers"></a><a id="COMADMININSTALLUSERS"></a><dl>
<dt><b>COMAdminInstallUsers</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Install users saved in an application file.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminInstallForceOverwriteOfFiles"></a><a id="comadmininstallforceoverwriteoffiles"></a><a id="COMADMININSTALLFORCEOVERWRITEOFFILES"></a><dl>
<dt><b>COMAdminInstallForceOverwriteOfFiles</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Overwrite files.

</td>
</tr>
</table>

### -param bstrUserId [in, optional]

The user ID under which to run the application.

### -param bstrPassword [in, optional]

The password under which to run the application.

### -param bstrRSN [in, optional]

A remote server name to use for an application proxy.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
A fatal error occurred during installation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_OBJECT_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The application does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_OBJECTERRORS</b></dt>
</dl>
</td>
<td width="60%">
An error occurred accessing one or more objects.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>
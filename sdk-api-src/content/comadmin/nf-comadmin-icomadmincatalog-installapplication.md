---
UID: NF:comadmin.ICOMAdminCatalog.InstallApplication
title: ICOMAdminCatalog::InstallApplication
author: windows-driver-content
description: Installs a COM+ application or application proxy from the specified file.
old-location: cos\icomadmincatalog_installapplication.htm
old-project: cossdk
ms.assetid: 668f73e1-7238-42f5-b68c-a0b0c2595d18
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: COMAdminInstallForceOverwriteOfFiles, COMAdminInstallNoUsers, COMAdminInstallUsers, ICOMAdminCatalog interface [COM+],InstallApplication method, ICOMAdminCatalog.InstallApplication, ICOMAdminCatalog::InstallApplication, InstallApplication, InstallApplication method [COM+], InstallApplication method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_InstallApplication, comadmin/ICOMAdminCatalog::InstallApplication, cos.icomadmincatalog_installapplication
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComAdmin.h
api_name:
-	ICOMAdminCatalog.InstallApplication
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 


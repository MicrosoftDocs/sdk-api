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
 

 


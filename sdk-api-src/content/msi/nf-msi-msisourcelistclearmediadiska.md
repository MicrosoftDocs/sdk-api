---
UID: NF:msi.MsiSourceListClearMediaDiskA
title: MsiSourceListClearMediaDiskA function
author: windows-sdk-content
description: The MsiSourceListClearMediaDisk function provides the ability to remove an existing registered disk under the media source for a product or patch in a specific context.
old-location: setup\msisourcelistclearmediadisks.htm
old-project: Msi
ms.assetid: e2e7cc95-e41b-4270-8650-30a1c12a0057
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: MSICODE_PATCH, MSICODE_PRODUCT, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiSourceListClearMediaDisk, MsiSourceListClearMediaDisk function, MsiSourceListClearMediaDiskA, MsiSourceListClearMediaDiskW, NULL, User SID, msi/MsiSourceListClearMediaDisk, msi/MsiSourceListClearMediaDiskA, msi/MsiSourceListClearMediaDiskW, setup.msisourcelistclearmediadisks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.0 or later on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSourceListClearMediaDiskW (Unicode) and MsiSourceListClearMediaDiskA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRM_LICENSE_ACQ_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiSourceListClearMediaDisk
-	MsiSourceListClearMediaDiskA
-	MsiSourceListClearMediaDiskW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiSourceListClearMediaDiskA function


## -description


 The <b>MsiSourceListClearMediaDisk</b> function provides the ability to remove an existing registered disk under the media source for a product or patch in a specific context.   
			
		


## -parameters




### -param szProductCodeOrPatchCode [in]

The <a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a> or patch GUID of the product or patch. Use a null-terminated string. If the string is longer than 39 characters, the function fails and returns ERROR_INVALID_PARAMETER. This parameter cannot be <b>NULL</b>.


### -param szUserSid [in, optional]

 This parameter can be a string SID that specifies the user account that contains the product or patch.  The SID is not validated or resolved. An incorrect SID can return ERROR_UNKNOWN_PRODUCT or ERROR_UNKNOWN_PATCH. 

<table>
<tr>
<th>Type of SID</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b><b>NULL</b></b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> denotes the currently logged on user.  When referencing the current user account, <i>szUserSID</i> can be <b>NULL</b> and <i>dwContext</i> can be  MSIINSTALLCONTEXT_USERMANAGED or MSIINSTALLCONTEXT_USERUNMANAGED.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
Specifies enumeration for a particular user in the system.  An example of user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string s-1-5-18 (system) cannot be used to enumerate products or patches installed as per-machine.  Setting the SID value to s-1-5-18 returns ERROR_INVALID_PARAMETER. When <i>dwContext</i> is set to MSIINSTALLCONTEXT_MACHINE only, <i>szUserSid</i> must be <b>NULL</b>. 
</div>
<div> </div>
<div class="alert"><b>Note</b>  The special SID string s-1-1-0 (everyone) should not be used. Setting the SID value to s-1-1-0 fails and returns ERROR_INVALID_PARAM.</div>
<div> </div>

### -param dwContext [in]

This parameter specifies the context of the product or patch instance. This parameter can contain one of the following values.   

<table>
<tr>
<th>Type of context</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
</dl>
</td>
<td width="60%">
The product or patch instance exists in the per-user-managed context. 

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
</dl>
</td>
<td width="60%">
 The product or patch instance exists in the  per-user-unmanaged context.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
The product or patch instance exists in the per-machine context.

</td>
</tr>
</table>
 


### -param dwOptions [in]

The <i>dwOptions</i> value specifies the meaning of <i>szProductCodeOrPatchCode</i>.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSICODE_PRODUCT"></a><a id="msicode_product"></a><dl>
<dt><b>MSICODE_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
<i>szProductCodeOrPatchCode</i> is a product code GUID. 



							

</td>
</tr>
<tr>
<td width="40%"><a id="MSICODE_PATCH"></a><a id="msicode_patch"></a><dl>
<dt><b>MSICODE_PATCH</b></dt>
</dl>
</td>
<td width="60%">
<i>szProductCodeOrPatchCode</i> is a patch code GUID.

</td>
</tr>
</table>
 


### -param dwDiskId

TBD




#### - dwDiskID [in]

This parameter provides the ID of the disk being removed.  


## -returns




					The <b>MsiSourceListClearMediaDisk</b> function returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have the ability to read the specified media source or the specified product or patch. This does not indicate whether a media source, product or patch was found.

</td>
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
<dt><b>ERROR_INSTALL_SERVICE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The Windows Installer service could not be accessed.

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
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The value was successfully removed or not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PATCH</b></dt>
</dl>
</td>
<td width="60%">
The patch was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected internal failure.

</td>
</tr>
</table>
 




## -remarks



Administrators can modify the installation  of   a product or patch   instance that exists  under the machine context or under their own per-user context (managed or unmanaged.) They can modify the installation of  a product or patch instance that exists under any user's per-user-managed context.  Administrators cannot modify another user's installation of a product or patch instance  that exists  under that other user's per-user-unmanaged context. 

Non-administrators cannot  modify the installation of  a product or patch instance that exists under another user's per-user context (managed or unmanaged.) They can modify the installation of  a product or patch instance that exists under their own per-user-unmanaged context.  They can modify the installation of a product or patch instance under the machine context or their own per-user-managed context only if they are enabled to browse for a product or patch source. Users can be enabled to browse for sources by setting policy. For more information, see the <a href="https://msdn.microsoft.com/51806a4c-4ae5-42e9-9d58-8032108164cb">DisableBrowse</a>, <a href="https://msdn.microsoft.com/1cf83f77-75a4-48c3-961e-339c76ba4306">AllowLockdownBrowse</a>, and <a href="https://msdn.microsoft.com/0bbec06a-0a2b-430a-a361-317a319da615">AlwaysInstallElevated</a> policies.




## -see-also




<a href="https://msdn.microsoft.com/850b598a-338e-4f84-8336-01e962256a08">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a>
 

 


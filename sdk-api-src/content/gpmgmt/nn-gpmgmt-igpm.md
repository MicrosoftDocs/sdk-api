---
UID: NN:gpmgmt.IGPM
title: IGPM
author: windows-sdk-content
description: The IGPM interface provides methods that access other interfaces of the Group Policy Management Console (GPMC) and methods that create other objects on which various search operations can be performed.
old-location: gpmc\igpm.htm
tech.root: GPMC
ms.assetid: 2780760e-7114-46b0-a264-00ed58a556cb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GPM, IGPM, IGPM interface [GPMC], IGPM interface [GPMC],described, _win32_igpm, gpmc.igpm, gpmgmt/IGPM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPM
 - GPM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPM interface


## -description


The 
<b>IGPM</b> interface provides methods that access other interfaces of the Group Policy Management Console (GPMC) and methods that create other objects on which various search operations can be performed.

The <b>GPM</b> object is the only object used with 
the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPM</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPM</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGPM</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">CreatePermission</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">GPMPermission</a> object which supports methods that retrieve multiple permission-related properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bb99109-c0d6-47cb-9ea4-6c60c1607b79">CreateSearchCriteria</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">GPMSearchCriteria</a> object which represents the criteria to use for search operations when using the GPMC interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98230e5f-b866-4f68-9977-eec4bdd14d9e">CreateTrustee</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">GPMTrustee</a> object from which you can retrieve information about a trustee.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae9ea50f-d652-4d7a-aac5-5b9ef27b99e0">CreatMigrationTable</a>
</td>
<td align="left" width="63%">
Creates an empty migration table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ffc8827-8427-4ee5-ad89-21f821d16d97">GetBackupDir</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">GPMBackupDir</a> object which you can use to access 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> and 
<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">GPMBackupCollection</a> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bcf76f5-f216-4a33-9ac1-4cb98eb26db5">GetClientSideExtensions</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://msdn.microsoft.com/e32c1c39-b817-4db6-ad76-b2e66b54d79d">GPMCSECollection</a> object that allows you to enumerate the Group Policy client-side extensions (CSEs) that are registered on the local computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba271dbb-320f-409c-aff4-b7dde57f9062">GetConstants</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">GPMConstants</a> object which supports methods that retrieve the value of multiple GPMC constants.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32aee72f-96fa-4ebd-9ff7-643972b82cf6">GetDomain</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">GPMDomain</a> object, which allows you to create, query, and restore Group Policy objects (GPOs), and to search scope of management (SOM) objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a39d4f8-777d-4cf8-8dd5-053f73bdfdfa">GetMigrationTable</a>
</td>
<td align="left" width="63%">
Loads the migration table at a specified path, and returns a <a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">GPMMigrationTable</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61a1be3e-d959-47e2-ad6c-ca00accd0afe">GetRSOP</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">GPMRSOP</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a1b8975-cd73-49e6-83b9-f6af296276cb">GetSitesContainer</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://msdn.microsoft.com/e3fdfd44-9e90-4206-b7e9-97d4ed6eb8af">GPMSitesContainer</a> object from which sites in a forest can be opened and queried.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e9f6ac5-d6d7-4360-b722-0b22e2391d20">InitializeReporting</a>
</td>
<td align="left" width="63%">
Sets the location of .adm files that are specified by the user, and initiates reporting.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a02e9261-8bf5-4e1e-ae3f-64a763f93751">GPMC Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 


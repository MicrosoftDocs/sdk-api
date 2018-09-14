---
UID: NN:gpmgmt.IGPMGPO
title: IGPMGPO
author: windows-sdk-content
description: The IGPMGPO interface supports methods that enable you to manage Group Policy Objects (GPOs) in the directory service.
old-location: gpmc\igpmgpo.htm
tech.root: GPMC
ms.assetid: 2857c8b7-019d-4ec2-9a00-574fc8541cae
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GPMGPO, IGPMGPO, IGPMGPO interface [GPMC], IGPMGPO interface [GPMC],described, _win32_igpmgpo, gpmc.igpmgpo, gpmgmt/ IGPMGPO
ms.prod: windows
ms.technology: windows-sdk
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
 - IGPMGPO
 - GPMGPO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMGPO interface


## -description


The 
<b>IGPMGPO</b> interface supports methods that enable you to manage Group Policy Objects (GPOs) in the directory service.

Note that you cannot use this interface to manage local GPOs (LGPOs).

You can instantiate a <b>GPMGPO</b> object by creating a new one with a call to 
<a href="https://msdn.microsoft.com/00e83637-820b-488e-abf4-4210ac3b98b6">IGPMDomain::CreateGPO</a>, retrieving an existing one with a call to 
<a href="https://msdn.microsoft.com/ac413241-3649-4f22-9a67-94e4da8672e7">IGPMDomain::GetGPO</a>, or by searching for one with a call to 
<a href="https://msdn.microsoft.com/19a8efae-0b85-49ba-bf7e-08ed700874c3">IGPMDomain::SearchGPOs</a>. After creating the object, you can query the GPO and set properties related to the GPO.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n"> IGPMGPO</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b> IGPMGPO</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b> IGPMGPO</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ba8d2f7-4989-4882-9ceb-4f77b8745442">Backup</a>
</td>
<td align="left" width="63%">
Backs up the GPO to the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17f4c6b2-6c75-4d4c-88c5-6d9ef2cb7a07">CopyTo</a>
</td>
<td align="left" width="63%">
Copies the policy settings from the GPO in the current domain to a new GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63a29bf5-bac5-43af-87ec-01c3c2a5b3af">Delete</a>
</td>
<td align="left" width="63%">
Deletes the GPO from the directory service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19b3b027-59f1-4c31-896b-5b5fd23b9be4">GenerateReport</a>
</td>
<td align="left" width="63%">
Generates a report for a GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/686b1461-3136-4351-adc4-32d558d62246">GenerateReportToFile</a>
</td>
<td align="left" width="63%">
Generates a report for a GPO and then saves the report to a file in a specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4035119b-2688-4326-8d08-825d53c3d8e2">GetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IDispatch</b> interface from which the security descriptor for the GPO can be retrieved. For script programmers, returns a reference to an 
<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/104e96e6-60c5-4cc1-9728-7c0ea9715a58">GetSecurityInfo</a>
</td>
<td align="left" width="63%">
Retrieves the set of permissions for the GPO, such as who is granted the rights to edit it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eca1dffb-1e92-42a1-b950-c6c6c88bd064">GetWMIFilter</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">GPMWMIFilter</a> object that is linked to the current GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b16eefb-89af-408b-a84c-c8ab958b4cc7">Import</a>
</td>
<td align="left" width="63%">
Imports the policy settings in the specified 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a4f2d87-bfaa-453a-9dbe-de19ba1d1953">IsACLConsistent</a>
</td>
<td align="left" width="63%">
Checks the consistency of 
<a href="https://msdn.microsoft.com/c9aff246-fe11-4d82-b944-b10c3d9ae170">access control lists</a> (ACLs) between the Directory Service and the system volume folder (SYSVOL).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5e235a0-dc12-4ff5-a3ca-0f3492edb713">IsComputerEnabled</a>
</td>
<td align="left" width="63%">
Determines whether the computer settings in the GPO are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5ed21bd-19b7-4518-97fa-6ffcd4ea80b4">IsUserEnabled</a>
</td>
<td align="left" width="63%">
Determines whether the user settings in the GPO are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/936e7795-e5ab-4014-86df-6b74ab122b11">MakeACLConsistent</a>
</td>
<td align="left" width="63%">
Makes <a href="https://msdn.microsoft.com/c9aff246-fe11-4d82-b944-b10c3d9ae170">ACLs</a> consistent between the Directory Service and the system volume folder (SYSVOL).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22d6fd46-9d6f-455e-8f01-96fc3f44b335">SetComputerEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables the computer policy settings in the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/087cbe19-25d9-4134-8893-1b2906915220">SetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Sets the security descriptor for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52b55e05-6107-4fa7-9991-55550393fee5">SetSecurityInfo</a>
</td>
<td align="left" width="63%">
Sets the list of permissions for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25a86f15-a5b0-4412-931b-444f4a684dc6">SetUserEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables the user policy settings in the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd086bae-9436-4612-95d6-56fe431d2c51">SetWMIFilter</a>
</td>
<td align="left" width="63%">
Links the <a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">GPMWMIFilter</a> object to the current GPO.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n"> IGPMGPO</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1087a0b7-3b23-4bc1-aa4b-9cbd15a7b3f2">ComputerDSVersionNumber</a>


</td>
<td align="left" width="63%">
Version number of the directory service component of the computer configuration portion of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1087a0b7-3b23-4bc1-aa4b-9cbd15a7b3f2">ComputerSysvolVersionNumber</a>


</td>
<td align="left" width="63%">
Version number of the system volume folder (SYSVOL) component of the computer configuration portion of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1087a0b7-3b23-4bc1-aa4b-9cbd15a7b3f2">CreationTime</a>


</td>
<td align="left" width="63%">
Time when the GPO was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1087a0b7-3b23-4bc1-aa4b-9cbd15a7b3f2">DisplayName</a>


</td>
<td align="left" width="63%">
Friendly display name of the GPO. More than one GPO can have the same display name. GPOs are identified in the Directory Service by the GPO ID, which is a GUID. GPOs are not identified in the Directory Service by the display name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1087a0b7-3b23-4bc1-aa4b-9cbd15a7b3f2">DomainName</a>


</td>
<td align="left" width="63%">
Domain name for the GPO. This is the full Domain Name System (DNS) name, for example, example.microsoft.com.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1087a0b7-3b23-4bc1-aa4b-9cbd15a7b3f2">ID</a>


</td>
<td align="left" width="63%">
ID of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1087a0b7-3b23-4bc1-aa4b-9cbd15a7b3f2">ModificationTime</a>


</td>
<td align="left" width="63%">
Time when the GPO was last modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1087a0b7-3b23-4bc1-aa4b-9cbd15a7b3f2">Path</a>


</td>
<td align="left" width="63%">
Distinguished name of the GPO in the Active Directory directory service; for example, cn={myguid},cn=policies,cn=system,dc=coname,dc=com.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1087a0b7-3b23-4bc1-aa4b-9cbd15a7b3f2">UserDSVersionNumber</a>


</td>
<td align="left" width="63%">
Version number of the directory service component of the user configuration portion of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1087a0b7-3b23-4bc1-aa4b-9cbd15a7b3f2">UserSysvolVersionNumber</a>


</td>
<td align="left" width="63%">
Version number of the system volume folder (SYSVOL) component of the user configuration portion of the GPO.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">IGPMGPOCollection</a>



<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>
 

 


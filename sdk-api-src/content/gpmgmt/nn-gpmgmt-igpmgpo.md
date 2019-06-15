---
UID: NN:gpmgmt.IGPMGPO
title: IGPMGPO (gpmgmt.h)
author: windows-sdk-content
description: The IGPMGPO interface supports methods that enable you to manage Group Policy Objects (GPOs) in the directory service.
old-location: gpmc\igpmgpo.htm
tech.root: gpmc
ms.assetid: 2857c8b7-019d-4ec2-9a00-574fc8541cae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMGPO, IGPMGPO, IGPMGPO interface [GPMC], IGPMGPO interface [GPMC],described, _win32_igpmgpo, gpmc.igpmgpo, gpmgmt/ IGPMGPO
ms.topic: interface
f1_keywords: ["gpmgmt/IGPMGPO"]
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
ms.custom: 19H1
---

# IGPMGPO interface


## -description


The 
<b>IGPMGPO</b> interface supports methods that enable you to manage Group Policy Objects (GPOs) in the directory service.

Note that you cannot use this interface to manage local GPOs (LGPOs).

You can instantiate a <b>GPMGPO</b> object by creating a new one with a call to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-creategpo">IGPMDomain::CreateGPO</a>, retrieving an existing one with a call to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-getgpo">IGPMDomain::GetGPO</a>, or by searching for one with a call to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-searchgpos">IGPMDomain::SearchGPOs</a>. After creating the object, you can query the GPO and set properties related to the GPO.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n"> IGPMGPO</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b> IGPMGPO</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-backup">Backup</a>
</td>
<td align="left" width="63%">
Backs up the GPO to the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-copyto">CopyTo</a>
</td>
<td align="left" width="63%">
Copies the policy settings from the GPO in the current domain to a new GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the GPO from the directory service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-generatereport">GenerateReport</a>
</td>
<td align="left" width="63%">
Generates a report for a GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-generatereporttofile">GenerateReportToFile</a>
</td>
<td align="left" width="63%">
Generates a report for a GPO and then saves the report to a file in a specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-getsecuritydescriptor">GetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IDispatch</b> interface from which the security descriptor for the GPO can be retrieved. For script programmers, returns a reference to an 
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-getsecurityinfo">GetSecurityInfo</a>
</td>
<td align="left" width="63%">
Retrieves the set of permissions for the GPO, such as who is granted the rights to edit it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-getwmifilter">GetWMIFilter</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object that is linked to the current GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-import">Import</a>
</td>
<td align="left" width="63%">
Imports the policy settings in the specified 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-isaclconsistent">IsACLConsistent</a>
</td>
<td align="left" width="63%">
Checks the consistency of 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control-lists">access control lists</a> (ACLs) between the Directory Service and the system volume folder (SYSVOL).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-iscomputerenabled">IsComputerEnabled</a>
</td>
<td align="left" width="63%">
Determines whether the computer settings in the GPO are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-isuserenabled">IsUserEnabled</a>
</td>
<td align="left" width="63%">
Determines whether the user settings in the GPO are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-makeaclconsistent">MakeACLConsistent</a>
</td>
<td align="left" width="63%">
Makes <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> consistent between the Directory Service and the system volume folder (SYSVOL).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-setcomputerenabled">SetComputerEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables the computer policy settings in the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-setsecuritydescriptor">SetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Sets the security descriptor for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-setsecurityinfo">SetSecurityInfo</a>
</td>
<td align="left" width="63%">
Sets the list of permissions for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-setuserenabled">SetUserEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables the user policy settings in the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-setwmifilter">SetWMIFilter</a>
</td>
<td align="left" width="63%">
Links the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object to the current GPO.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpo-property-methods">ComputerDSVersionNumber</a>


</td>
<td align="left" width="63%">
Version number of the directory service component of the computer configuration portion of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpo-property-methods">ComputerSysvolVersionNumber</a>


</td>
<td align="left" width="63%">
Version number of the system volume folder (SYSVOL) component of the computer configuration portion of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpo-property-methods">CreationTime</a>


</td>
<td align="left" width="63%">
Time when the GPO was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpo-property-methods">DisplayName</a>


</td>
<td align="left" width="63%">
Friendly display name of the GPO. More than one GPO can have the same display name. GPOs are identified in the Directory Service by the GPO ID, which is a GUID. GPOs are not identified in the Directory Service by the display name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpo-property-methods">DomainName</a>


</td>
<td align="left" width="63%">
Domain name for the GPO. This is the full Domain Name System (DNS) name, for example, example.microsoft.com.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpo-property-methods">ID</a>


</td>
<td align="left" width="63%">
ID of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpo-property-methods">ModificationTime</a>


</td>
<td align="left" width="63%">
Time when the GPO was last modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpo-property-methods">Path</a>


</td>
<td align="left" width="63%">
Distinguished name of the GPO in the Active Directory directory service; for example, cn={myguid},cn=policies,cn=system,dc=coname,dc=com.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpo-property-methods">UserDSVersionNumber</a>


</td>
<td align="left" width="63%">
Version number of the directory service component of the user configuration portion of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmgpo-property-methods">UserSysvolVersionNumber</a>


</td>
<td align="left" width="63%">
Version number of the system volume folder (SYSVOL) component of the user configuration portion of the GPO.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMGPOCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>
 

 


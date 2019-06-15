---
UID: NN:gpmgmt.IGPMStarterGPO
title: IGPMStarterGPO (gpmgmt.h)
author: windows-sdk-content
description: The IGPMStarterGPO interface supports methods that enable you to manage Starter Group Policy Objects (GPOs) in the directory service.
old-location: gpmc\igpmstartergpo.htm
tech.root: gpmc
ms.assetid: 5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGPMStarterGPO, IGPMStarterGPO interface [GPMC], IGPMStarterGPO interface [GPMC],described, gpmc.igpmstartergpo, gpmgmt/IGPMStarterGPO
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
 - IGPMStarterGPO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMStarterGPO interface


## -description


The 
<b>IGPMStarterGPO</b> interface supports methods that enable you to manage Starter Group Policy Objects (GPOs) in the directory service.

Note that you cannot use this interface to manage local GPOs (LGPOs).

You can instantiate a <b>GPMStarterGPO</b> object by creating a new one with a call to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain2-createstartergpo">IGPMDomain2::CreateStarterGPO</a>, retrieving an existing one with a call to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain2-getstartergpo">IGPMDomain2::GetStarterGPO</a>, or by searching for one with a call to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain2-searchstartergpos">IGPMDomain2::SearchStarterGPOs</a>. After creating the object, you can query the GPO and set properties related to the GPO.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPO</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMStarterGPO</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMStarterGPO</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpo-backup">Backup</a>
</td>
<td align="left" width="63%">
Backs up the Starter GPO to the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpo-copyto">CopyTo</a>
</td>
<td align="left" width="63%">
Copies the policy settings from the Starter GPO in the current domain to a new Starter GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpo-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the Starter GPO from the directory service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpo-generatereport">GenerateReport</a>
</td>
<td align="left" width="63%">
Generates a report for a Starter GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpo-generatereporttofile">GenerateReportToFile</a>
</td>
<td align="left" width="63%">
Generates a report for a Starter GPO and saves it to a file at a specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpo-getsecurityinfo">GetSecurityInfo</a>
</td>
<td align="left" width="63%">
Retrieves the set of permissions for the GPO, such as who is granted the rights to edit it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpo-save">Save</a>
</td>
<td align="left" width="63%">
Saves all the Starter GPO settings in a single CAB file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpo-setsecurityinfo">SetSecurityInfo</a>
</td>
<td align="left" width="63%">
Sets the list of permissions for the GPO.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPO</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">Author</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the person who created the Starter GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">ComputerVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Version number of the computer configuration portion of the Starter GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">CreationTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Time when the Starter GPO was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Starter GPO comment or description.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">DisplayName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Friendly display name of the Starter GPO. Starter GPOs are identified in the Directory Service by ID (GUID), not by friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">ID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
ID of the Starter GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">ModifiedTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Time when the Starter GPO was last modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">Product</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the product this Starter GPO is designed  to manage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">StarterGPOVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Version number of the Starter GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the type of Starter GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">UserVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Version number of the user configuration portion of the Starter GPO.

</td>
</tr>
</table> 


## -remarks



The <b>GPMStarterGPO</b> object is analogous to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo2">GPMGPO2</a> object. The <b>GPMStarterGPO</b> object represents a single instance of a Starter Group Policy object (GPO).

The <b>IGPMStarterGPO</b> interface has three properties that do not have a counterpart in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo2">IGPMGPO2</a> interface.

<ul>
<li>The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">Author</a> property contains the name of who created the Template.  This attribute is applicable to System Templates.  For custom Templates this attribute will be blank.  This attribute is read-only.</li>
<li>The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">Product</a> 
     property contains the name of the product that the Template is designed to manage.  For example a Template might ship to configure MS Office.  This attribute is applicable to System Templates.  For custom Templates this attribute will be blank.  This attribute is read-only.</li>
<li>The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpo-property-methods">Type</a> 
     property is an enum value,  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/ne-gpmgmt-__midl___midl_itf_gpmgmt_0000_0030_0002">GPMStarterGPOType</a>, that specifies the type of the attribute.  The Type may be either a system  Starter Group Policy object or a custom Starter Group Policy object.</li>
</ul>
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpo-save">Save</a> method has no corresponding method in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo2">IGPMGPO2</a> interface.  The <b>Save</b> method will generate a CAB file containing all the contents of a single Starter GPO.  The objective of this method is to allow a user to save a Starter GPO in a form that can be easily redistributed. There is no way to create a CAB file containing multiple Starter GPOs.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm2">IGPM2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain2">IGPMDomain2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">IGPMStarterGPOBackup</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpocollection">IGPMStarterGPOCollection</a>
 

 


---
UID: NN:gpmgmt.IGPMStarterGPO
title: IGPMStarterGPO
author: windows-sdk-content
description: The IGPMStarterGPO interface supports methods that enable you to manage Starter Group Policy Objects (GPOs) in the directory service.
old-location: gpmc\igpmstartergpo.htm
old-project: GPMC
ms.assetid: 5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IGPMStarterGPO, IGPMStarterGPO interface [GPMC], IGPMStarterGPO interface [GPMC],described, gpmc.igpmstartergpo, gpmgmt/IGPMStarterGPO
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMStarterGPO
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMStarterGPO interface


## -description


The 
<b>IGPMStarterGPO</b> interface supports methods that enable you to manage Starter Group Policy Objects (GPOs) in the directory service.

Note that you cannot use this interface to manage local GPOs (LGPOs).

You can instantiate a <b>GPMStarterGPO</b> object by creating a new one with a call to 
<a href="https://msdn.microsoft.com/652ac85b-f488-4e27-81dd-1ffc5f9f42d6">IGPMDomain2::CreateStarterGPO</a>, retrieving an existing one with a call to 
<a href="https://msdn.microsoft.com/0648c653-94da-40d6-98c2-46f80a51bc90">IGPMDomain2::GetStarterGPO</a>, or by searching for one with a call to 
<a href="https://msdn.microsoft.com/30a325e8-372a-4e30-a420-10f5b6ef295d">IGPMDomain2::SearchStarterGPOs</a>. After creating the object, you can query the GPO and set properties related to the GPO.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPO</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGPMStarterGPO</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/bf419f56-803f-44c2-ae08-7e428940f79d">Backup</a>
</td>
<td align="left" width="63%">
Backs up the Starter GPO to the specified directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28639323-5253-4f63-b1b1-4fd75abaa2b4">CopyTo</a>
</td>
<td align="left" width="63%">
Copies the policy settings from the Starter GPO in the current domain to a new Starter GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1392326e-68f0-4d55-8a6b-3abbb60b51ee">Delete</a>
</td>
<td align="left" width="63%">
Deletes the Starter GPO from the directory service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/127cde40-abe0-42da-9845-2fe1c0b1f1f1">GenerateReport</a>
</td>
<td align="left" width="63%">
Generates a report for a Starter GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29302091-0f2d-4511-a25b-9af078795d1d">GenerateReportToFile</a>
</td>
<td align="left" width="63%">
Generates a report for a Starter GPO and saves it to a file at a specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c411851-0902-454a-9b44-383ea572ab78">GetSecurityInfo</a>
</td>
<td align="left" width="63%">
Retrieves the set of permissions for the GPO, such as who is granted the rights to edit it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
Saves all the Starter GPO settings in a single CAB file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad4df57f-29b3-4a18-922a-a0d4457703ad">SetSecurityInfo</a>
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

<a href="https://msdn.microsoft.com/2cc1d707-d269-40ff-9356-c3ac2fa36de1">Author</a>


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

<a href="https://msdn.microsoft.com/2cc1d707-d269-40ff-9356-c3ac2fa36de1">ComputerVersion</a>


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

<a href="https://msdn.microsoft.com/2cc1d707-d269-40ff-9356-c3ac2fa36de1">CreationTime</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh965535">DisplayName</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">ID</a>


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

<a href="https://msdn.microsoft.com/2cc1d707-d269-40ff-9356-c3ac2fa36de1">ModifiedTime</a>


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

<a href="https://msdn.microsoft.com/2cc1d707-d269-40ff-9356-c3ac2fa36de1">Product</a>


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

<a href="https://msdn.microsoft.com/2cc1d707-d269-40ff-9356-c3ac2fa36de1">StarterGPOVersion</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


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

<a href="https://msdn.microsoft.com/2cc1d707-d269-40ff-9356-c3ac2fa36de1">UserVersion</a>


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



The <b>GPMStarterGPO</b> object is analogous to the <a href="https://msdn.microsoft.com/c5c21ca6-2722-4821-8760-03b6cf2befa7">GPMGPO2</a> object. The <b>GPMStarterGPO</b> object represents a single instance of a Starter Group Policy object (GPO).

The <b>IGPMStarterGPO</b> interface has three properties that do not have a counterpart in the <a href="https://msdn.microsoft.com/c5c21ca6-2722-4821-8760-03b6cf2befa7">IGPMGPO2</a> interface.

<ul>
<li>The <a href="https://msdn.microsoft.com/2cc1d707-d269-40ff-9356-c3ac2fa36de1">Author</a> property contains the name of who created the Template.  This attribute is applicable to System Templates.  For custom Templates this attribute will be blank.  This attribute is read-only.</li>
<li>The <a href="https://msdn.microsoft.com/2cc1d707-d269-40ff-9356-c3ac2fa36de1">Product</a> 
     property contains the name of the product that the Template is designed to manage.  For example a Template might ship to configure MS Office.  This attribute is applicable to System Templates.  For custom Templates this attribute will be blank.  This attribute is read-only.</li>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> 
     property is an enum value,  <a href="https://msdn.microsoft.com/19b84c06-d8dc-4a25-85f6-cfbe9937f30e">GPMStarterGPOType</a>, that specifies the type of the attribute.  The Type may be either a system  Starter Group Policy object or a custom Starter Group Policy object.</li>
</ul>
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a> method has no corresponding method in the <a href="https://msdn.microsoft.com/c5c21ca6-2722-4821-8760-03b6cf2befa7">IGPMGPO2</a> interface.  The <b>Save</b> method will generate a CAB file containing all the contents of a single Starter GPO.  The objective of this method is to allow a user to save a Starter GPO in a form that can be easily redistributed. There is no way to create a CAB file containing multiple Starter GPOs.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/f9cd432a-3974-4fc4-9e32-1d8e2df1601c">IGPM2</a>



<a href="https://msdn.microsoft.com/5abfea14-0cb9-46ea-915c-93a8d8b2477b">IGPMDomain2</a>



<a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">IGPMStarterGPOBackup</a>



<a href="https://msdn.microsoft.com/b650b1c6-0597-468a-afdc-a21d61f1a8a0">IGPMStarterGPOCollection</a>
 

 


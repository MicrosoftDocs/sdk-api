---
UID: NN:fsrmpipeline.IFsrmPropertyBag
title: IFsrmPropertyBag (fsrmpipeline.h)
author: windows-sdk-content
description: Contains the classification properties for a file.
old-location: fsrm\ifsrmpropertybag.htm
tech.root: fsrm
ms.assetid: 237f024d-2b1d-45d5-a63d-c530426278e6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmPropertyBag, IFsrmPropertyBag interface [File Server Resource Manager], IFsrmPropertyBag interface [File Server Resource Manager],described, fs.ifsrmpropertybag, fsrm.ifsrmpropertybag, fsrm/IFsrmPropertyBag
ms.topic: interface
req.header: fsrmpipeline.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmPropertyBag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmPropertyBag interface


## -description


Contains the classification properties for a file.

FSRM passes this interface to your 
    <a href="https://msdn.microsoft.com/a4420b1e-e2e5-460c-948c-3c5f97d7a0e7">IFsrmPipelineModuleImplementation</a> 
    implementation. For more information, see the Remarks section.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPropertyBag</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFsrmPropertyBag</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmPropertyBag</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d9166fd-5211-4114-843f-2c6563941715">AddMessage</a>
</td>
<td align="left" width="63%">
Adds a message about the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09fc3287-f2a2-4ba7-9626-65c6634b7f2d">GetFileProperty</a>
</td>
<td align="left" width="63%">
Retrieves the specified metadata property of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5250f0f-c8b4-4579-a4c2-b4f6ee48acdc">GetFileStreamInterface</a>
</td>
<td align="left" width="63%">
Retrieves a file stream interface that you can use to access the contents of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3322907-c832-49ef-bf21-2e4581251a88">SetFileProperty</a>
</td>
<td align="left" width="63%">
Sets the specified metadata property of the file.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPropertyBag</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9d84b68f-1db8-43d5-964b-c961ec9c250b">Attributes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The attributes of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/85953042-eeb6-49bd-bde0-f18d4edf108a">CreationTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The date and time that the file was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dc5df8d8-4998-4a4e-814b-f3119a156e14">FileId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The file identifier of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5dfbf1a8-99a4-4348-8fc4-9d582330be57">FilePropertyNames</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A list of the names of the file's metadata properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b17da883-7f8c-4df0-9ee2-7e75b5852aa9">LastAccessTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The date and time of when the file was last accessed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0afba4f9-b716-49dc-bbeb-6245e5c7a386">LastModificationTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The date and time of when the file was last modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3aa6bc28-03bb-40ea-8c56-94133c8eeb54">Messages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A list of the classification messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b500b16f-402d-475f-9de3-a54da1afb203">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bb2b0872-9553-40d3-a9b0-7602266c28da">OwnerSid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The SID of the owner of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a62f9562-06ba-41bc-8450-300dd50ee728">ParentDirectoryId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The identifier of the file's parent directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b7e5885e-c716-4fa8-afc0-bfe258e5f421">PropertyBagFlags</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A set of flags that provide additional information about the property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/31e0baad-286a-42f3-bd30-84fc40c935f6">RelativeNamespaceRoot</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The relative path of the namespace root under which the file is being evaluated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4304228a-5e8e-4e2d-9fc9-48777cb23251">RelativePath</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The relative path to the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6dade17c-1252-4f11-81a2-7e278da290e8">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The size of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d1ec946b-2769-4e0d-b01c-08ef6032df16">SizeAllocated</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The allocation size of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/08d4e052-710b-4f41-86b1-473760a6e9c6">VolumeIndex</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The index that the scanner uses to refer to the volume on which the file exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/65b47ad3-eb81-468e-a4fb-8a52d6b99998">VolumeName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name of the volume on which the file exists.

</td>
</tr>
</table> 


## -remarks



A property bag contains an in-memory copy of all the properties for a file. The list of properties in the 
    property bag may include additional properties not defined in FSRM. These properties can be the result of other 
    metadata in the file.

This interface can be sent to 
    <a href="https://msdn.microsoft.com/ab42430c-1e30-4576-b6f8-c0488b6230dd">IFsrmClassifierModuleImplementation::DoesPropertyValueApply</a> 
    and 
    <a href="https://msdn.microsoft.com/70277473-de96-40e1-980b-4eec6e7b035d">IFsrmClassifierModuleImplementation::GetPropertyValueToApply</a> 
    if a classifier module is implemented, or to 
    <a href="https://msdn.microsoft.com/05de6dfe-0f90-4866-bedc-72b8fea9dfac">IFsrmStorageModuleImplementation::LoadProperties</a> 
    and 
    <a href="https://msdn.microsoft.com/4d31db26-9d03-46f3-a902-401f9e0d9767">IFsrmStorageModuleImplementation::SaveProperties</a> 
    if a storage module is implemented.




## -see-also




<a href="https://msdn.microsoft.com/f238c446-b268-4600-b6e3-ec772a5f7575">IFsrmClassifierModuleImplementation</a>



<a href="https://msdn.microsoft.com/a4420b1e-e2e5-460c-948c-3c5f97d7a0e7">IFsrmPipelineModuleImplementation</a>



<a href="https://msdn.microsoft.com/8540f1f4-8ed1-4e4d-b940-3e232eb8c2d6">IFsrmStorageModuleImplementation</a>
 

 


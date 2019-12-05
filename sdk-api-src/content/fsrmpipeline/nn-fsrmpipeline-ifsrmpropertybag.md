---
UID: NN:fsrmpipeline.IFsrmPropertyBag
title: IFsrmPropertyBag (fsrmpipeline.h)
description: Contains the classification properties for a file.
old-location: fsrm\ifsrmpropertybag.htm
tech.root: fsrm
ms.assetid: 237f024d-2b1d-45d5-a63d-c530426278e6
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyBag, IFsrmPropertyBag interface [File Server Resource Manager], IFsrmPropertyBag interface [File Server Resource Manager],described, fs.ifsrmpropertybag, fsrm.ifsrmpropertybag, fsrm/IFsrmPropertyBag
ms.topic: interface
f1_keywords:
- fsrmpipeline/IFsrmPropertyBag
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmPropertyBag interface


## -description


Contains the classification properties for a file.

FSRM passes this interface to your 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleimplementation">IFsrmPipelineModuleImplementation</a> 
    implementation. For more information, see the Remarks section.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPropertyBag</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmPropertyBag</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-addmessage">AddMessage</a>
</td>
<td align="left" width="63%">
Adds a message about the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-getfileproperty">GetFileProperty</a>
</td>
<td align="left" width="63%">
Retrieves the specified metadata property of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-getfilestreaminterface">GetFileStreamInterface</a>
</td>
<td align="left" width="63%">
Retrieves a file stream interface that you can use to access the contents of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-setfileproperty">SetFileProperty</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_attributes">Attributes</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_creationtime">CreationTime</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_fileid">FileId</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_filepropertynames">FilePropertyNames</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_lastaccesstime">LastAccessTime</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_lastmodificationtime">LastModificationTime</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_messages">Messages</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_name">Name</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_ownersid">OwnerSid</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_parentdirectoryid">ParentDirectoryId</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_propertybagflags">PropertyBagFlags</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_relativenamespaceroot">RelativeNamespaceRoot</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_relativepath">RelativePath</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_size">Size</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_sizeallocated">SizeAllocated</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_volumeindex">VolumeIndex</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-get_volumename">VolumeName</a>


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
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-doespropertyvalueapply">IFsrmClassifierModuleImplementation::DoesPropertyValueApply</a> 
    and 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassifiermoduleimplementation-getpropertyvaluetoapply">IFsrmClassifierModuleImplementation::GetPropertyValueToApply</a> 
    if a classifier module is implemented, or to 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduleimplementation-loadproperties">IFsrmStorageModuleImplementation::LoadProperties</a> 
    and 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmstoragemoduleimplementation-saveproperties">IFsrmStorageModuleImplementation::SaveProperties</a> 
    if a storage module is implemented.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmpipelinemoduleimplementation">IFsrmPipelineModuleImplementation</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmstoragemoduleimplementation">IFsrmStorageModuleImplementation</a>
 

 


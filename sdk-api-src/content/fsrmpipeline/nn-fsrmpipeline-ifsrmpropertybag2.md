---
UID: NN:fsrmpipeline.IFsrmPropertyBag2
title: IFsrmPropertyBag2 (fsrmpipeline.h)
description: IFsrmPropertyBag2 Interface
helpviewer_keywords: ["IFsrmPropertyBag2","IFsrmPropertyBag2 interface [File Server Resource Manager]","IFsrmPropertyBag2 interface [File Server Resource Manager]","described","fs.ifsrmpropertybag2","fsrm.ifsrmpropertybag2","fsrmpipeline/IFsrmPropertyBag2"]
old-location: fsrm\ifsrmpropertybag2.htm
tech.root: fsrm
ms.assetid: 8f69556f-b96e-49b5-bc40-242768ebe767
ms.date: 12/05/2018
ms.keywords: IFsrmPropertyBag2, IFsrmPropertyBag2 interface [File Server Resource Manager], IFsrmPropertyBag2 interface [File Server Resource Manager],described, fs.ifsrmpropertybag2, fsrm.ifsrmpropertybag2, fsrmpipeline/IFsrmPropertyBag2
req.header: fsrmpipeline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmPipeline.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmPropertyBag2
 - fsrmpipeline/IFsrmPropertyBag2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmPropertyBag2
---

# IFsrmPropertyBag2 interface


## -description

IFsrmPropertyBag2 Interface

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPropertyBag2</b> interface inherits from <b>IFsrmPropertyBag</b>. <b>IFsrmPropertyBag2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmPropertyBag2</b> interface has these methods.
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag2-getfieldvalue">GetFieldValue</a>
</td>
<td align="left" width="63%">
Gets the value of the specified field from the property bag.

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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPropertyBag2</b> interface has these properties.
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

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>


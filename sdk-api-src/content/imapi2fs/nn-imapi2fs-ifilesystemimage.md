---
UID: NN:imapi2fs.IFileSystemImage
title: IFileSystemImage
author: windows-sdk-content
description: Use this interface to build a file system image, set session parameter, and import or export an image.
old-location: imapi\ifilesystemimage.htm
tech.root: imapi
ms.assetid: 0256f1d2-a3fb-45b2-bd84-e2b71148e4ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFileSystemImage, IFileSystemImage interface [IMAPI], IFileSystemImage interface [IMAPI],described, imapi.ifilesystemimage, imapi2fs/IFileSystemImage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImage interface


## -description


Use this interface to build a file system image, set session parameter, and import or export an image.

The file system directory hierarchy is built by adding directories and files to the root or child directories.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftFileSystemImage) for the class identifier and __uuidof(IFileSystemImage) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSystemImage</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFileSystemImage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSystemImage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9211b8af-9331-4d0d-a6f5-f52f8db42e8c"> ChooseImageDefaults</a>
</td>
<td align="left" width="63%">
Sets the default file system types and the image size based on the current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d327da0-d0b3-4fcf-9773-ff5ea1eeea1c"> ChooseImageDefaultsForMediaType</a>
</td>
<td align="left" width="63%">
Sets the default file system types and the image size based on the specified media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9536444b-60e4-456f-b6d8-07cf9a6f7848"> get_ISO9660InterchangeLevel</a>
</td>
<td align="left" width="63%">
Retrieves the ISO9660 compatibility level to use when creating the result image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd19c3ce-ef84-4f15-9032-679115b8b21f"> get_ISO9660InterchangeLevelsSupported</a>
</td>
<td align="left" width="63%">
Retrieves the supported ISO9660 compatibility levels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10c0b02e-965e-47ca-95f4-237c21b505ad"> get_MultisessionInterfaces</a>
</td>
<td align="left" width="63%">
Retrieves the list of multi-session interfaces for the optical media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7146ad88-071a-4df9-80f9-46e24b49286b"> get_StageFiles</a>
</td>
<td align="left" width="63%">
Determines if the file system should be staged before the burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c854a8db-730a-42a3-b50c-fb8fec271b57"> get_UDFRevision</a>
</td>
<td align="left" width="63%">
Retrieves the UDF revision level of the imported file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bfb770a-5a69-4980-94e2-4a3f65caa645"> put_ISO9660InterchangeLevel</a>
</td>
<td align="left" width="63%">
Sets the ISO9660 compatibility level of the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/632cd123-4e66-4ac3-891a-aa9d0c085b4f"> put_MultisessionInterfaces</a>
</td>
<td align="left" width="63%">
Sets the list of multi-session interfaces for the optical media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4b0e73b-6bef-44e1-b0b7-9a4e0fcc1370"> put_UDFRevision</a>
</td>
<td align="left" width="63%">
Sets the UDF revision level of the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1d1fc83-326e-4d9f-b771-c520ee956ed5">CalculateDiscIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves a string that identifies a disc and the sessions recorded on the disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27eadc99-46b6-40e1-91e0-b5c532536491">CreateDirectoryItem</a>
</td>
<td align="left" width="63%">
Create a directory item with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e90e367-e7c3-41db-a8c9-9b0220cf402b">CreateFileItem</a>
</td>
<td align="left" width="63%">
Create a file item with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f7d2438-5c80-4461-8b48-646f0ca44498">CreateResultImage</a>
</td>
<td align="left" width="63%">
Create the result object that contains the file system and file data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3a86e85-1ffd-47c1-9dba-0fc207d76a1a">Exists</a>
</td>
<td align="left" width="63%">
Checks for the existence of a given file or directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9721313-a2b0-4d91-af10-7932bd2d01be">get_BootImageOptions</a>
</td>
<td align="left" width="63%">
Retrieves the boot image that you want to add to the file-system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5d15478-e632-4e76-91e2-ee360dfccf19">get_ChangePoint</a>
</td>
<td align="left" width="63%">
Retrieves the change point identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc8e0606-8662-441f-b244-7d6b0be4c4e7">get_DirectoryCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of directories in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2545f85-84c9-4f01-98d7-fd6b37fcda5a">get_FileCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of files in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73bf563b-ad8f-4afe-95c6-3bac3c4dadba">get_FileSystemsSupported</a>
</td>
<td align="left" width="63%">
Retrieves the list of file system types that a client can use to build a file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7350de0b-683a-4363-9233-dbe40f637f2d">get_FileSystemsToCreate</a>
</td>
<td align="left" width="63%">
Retrieves the types of file systems to create when generating the result stream.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4942d86d-0cc7-4f4e-b257-dc59d3896b38">get_FreeMediaBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of blocks available for the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57d66dd3-2525-4102-bba7-00bad76a3d9c">get_ImportedVolumeName</a>
</td>
<td align="left" width="63%">
Retrieves the volume name provided from an imported file system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b43468a-f02c-4806-9f65-529dc6d8f20a">get_Root</a>
</td>
<td align="left" width="63%">
Retrieves the root directory item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f1faea7-4272-42da-afdf-3399c9dd629f">get_SessionStartBlock</a>
</td>
<td align="left" width="63%">
Retrieves the starting block address for the recording session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07139ef3-ffd5-4035-afa9-6212808a6fbc">get_StrictFileSystemCompliance</a>
</td>
<td align="left" width="63%">
Determines the compliance level for creating and developing the file-system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad9b4a68-5fef-4092-9cef-4b5ebd9c5093">get_UDFRevisionsSupported</a>
</td>
<td align="left" width="63%">
Retrieves a list of supported UDF revision levels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97f59440-112b-49ea-9f8e-97e8a831229d">get_UsedBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the number of blocks in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/106615e8-f1d4-4ac9-b96a-bcda204f5e2c">get_UseRestrictedCharacterSet</a>
</td>
<td align="left" width="63%">
Determines if file and directory names should be restricted to using only CP_ANSI characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95d5738b-a720-4f47-b3a0-97f7474b051a">get_VolumeName</a>
</td>
<td align="left" width="63%">
Retrieves the volume name for this file system image. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f41c273-d56a-4e8f-aa9f-e2a49741f7e3">get_VolumeNameISO9660</a>
</td>
<td align="left" width="63%">
Retrieves the volume name for the ISO9660 system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5300763d-9f2f-4562-bb5e-61fcf485b086">get_VolumeNameJoliet</a>
</td>
<td align="left" width="63%">
Retrieves the volume name for the Joliet system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d034f8cb-38f5-42ab-8952-e4a76dc1f27d">get_VolumeNameUDF</a>
</td>
<td align="left" width="63%">
Retrieves the volume name for the UDF system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89c4fd34-6651-4056-9939-201f404ea6ee">get_WorkingDirectory</a>
</td>
<td align="left" width="63%">
Retrieves the temporary directory in which stash files are built.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbac5b93-669f-45ea-9a3d-e2dd7f8bdcf6">GetDefaultFileSystemForImport</a>
</td>
<td align="left" width="63%">
Retrieves the file system to import by default.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/381be283-c877-44f0-9d96-b9e80a6aeec8">IdentifyFileSystemsOnDisc</a>
</td>
<td align="left" width="63%">
Retrieves a list of the different types of file systems on the optical media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87d654bc-f2c9-4a74-a822-352cdb242b5f">ImportFileSystem</a>
</td>
<td align="left" width="63%">
Imports the default file system on the current disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/737f1b5a-be70-4869-9ad0-a1373cb865d9">ImportSpecificFileSystem</a>
</td>
<td align="left" width="63%">
Import a specific file system from disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae5d659c-5da7-4478-b65f-64cbe227dbc5">LockInChangePoint</a>
</td>
<td align="left" width="63%">
Locks the file system information at the current change-point level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0556b72d-eabd-4649-b16b-fd66052504f4">put_BootImageOptions</a>
</td>
<td align="left" width="63%">
Sets the boot image that you want to add to the file-system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9bb2a86-2bdb-495e-ab5c-479667a211b2">put_FileSystemsToCreate</a>
</td>
<td align="left" width="63%">
Sets the file systems to create when generating the result stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ffa2736-6480-4bda-8144-b949bf43e580">put_FreeMediaBlocks</a>
</td>
<td align="left" width="63%">
Sets the maximum number of blocks available for the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0018d614-c936-41f1-8700-477aa259da2a">put_SessionStartBlock</a>
</td>
<td align="left" width="63%">
Sets the starting block address for the recording session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1040831b-0bda-40b7-ab6d-c914515f4e69">put_StageFiles</a>
</td>
<td align="left" width="63%">
Determines if the file system should be staged before the burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccbeba5a-39d5-43fd-8693-fee7cbbf5c8a">put_StrictFileSystemCompliance</a>
</td>
<td align="left" width="63%">
Determines the compliance level for creating and developing the file-system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de64ef3d-94b3-4d97-946e-8331c5a39f4b">put_UseRestrictedCharacterSet</a>
</td>
<td align="left" width="63%">
Determines if file and directory names should be restricted to using only CP_ANSI characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afb87eb1-5d14-413a-8830-2612920eac3d">put_VolumeName</a>
</td>
<td align="left" width="63%">
Sets the volume name for this file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfe37cfe-654d-4923-b667-e44be7ce4715">put_WorkingDirectory</a>
</td>
<td align="left" width="63%">
Sets the temporary directory in which stash files are built.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/852b88ed-6af7-4fe6-bf5f-831d55423130">RollbackToChangePoint</a>
</td>
<td align="left" width="63%">
Reverts the image back to the specified change point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/201e7390-68f3-48a4-9036-b07219fa3d80">SetMaxMediaBlocksFromDevice</a>
</td>
<td align="left" width="63%">
Set maximum number of blocks available based on the capabilities of the recorder.

</td>
</tr>
</table> 


## -remarks



To create the <b>CFileSystemImage</b> object in a script, use IMAPI2.MsftFileSystemImage as the program identifier when calling <b>CreateObject</b>.




## -see-also




<a href="https://msdn.microsoft.com/cff27ceb-d14a-48c2-941e-d27d6505e2c5">DFileSystemImageEvents</a>
 

 


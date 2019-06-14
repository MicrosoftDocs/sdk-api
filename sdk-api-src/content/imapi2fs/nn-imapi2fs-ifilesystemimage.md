---
UID: NN:imapi2fs.IFileSystemImage
title: IFileSystemImage (imapi2fs.h)
author: windows-sdk-content
description: Use this interface to build a file system image, set session parameter, and import or export an image.
old-location: imapi\ifilesystemimage.htm
tech.root: imapi
ms.assetid: 0256f1d2-a3fb-45b2-bd84-e2b71148e4ec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileSystemImage, IFileSystemImage interface [IMAPI], IFileSystemImage interface [IMAPI],described, imapi.ifilesystemimage, imapi2fs/IFileSystemImage
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
ms.custom: 19H1
---

# IFileSystemImage interface


## -description


Use this interface to build a file system image, set session parameter, and import or export an image.

The file system directory hierarchy is built by adding directories and files to the root or child directories.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftFileSystemImage) for the class identifier and __uuidof(IFileSystemImage) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSystemImage</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFileSystemImage</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-chooseimagedefaults"> ChooseImageDefaults</a>
</td>
<td align="left" width="63%">
Sets the default file system types and the image size based on the current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-chooseimagedefaultsformediatype"> ChooseImageDefaultsForMediaType</a>
</td>
<td align="left" width="63%">
Sets the default file system types and the image size based on the specified media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_iso9660interchangelevel"> get_ISO9660InterchangeLevel</a>
</td>
<td align="left" width="63%">
Retrieves the ISO9660 compatibility level to use when creating the result image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_iso9660interchangelevelssupported"> get_ISO9660InterchangeLevelsSupported</a>
</td>
<td align="left" width="63%">
Retrieves the supported ISO9660 compatibility levels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces"> get_MultisessionInterfaces</a>
</td>
<td align="left" width="63%">
Retrieves the list of multi-session interfaces for the optical media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_stagefiles"> get_StageFiles</a>
</td>
<td align="left" width="63%">
Determines if the file system should be staged before the burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_udfrevision"> get_UDFRevision</a>
</td>
<td align="left" width="63%">
Retrieves the UDF revision level of the imported file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_iso9660interchangelevel"> put_ISO9660InterchangeLevel</a>
</td>
<td align="left" width="63%">
Sets the ISO9660 compatibility level of the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces"> put_MultisessionInterfaces</a>
</td>
<td align="left" width="63%">
Sets the list of multi-session interfaces for the optical media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_udfrevision"> put_UDFRevision</a>
</td>
<td align="left" width="63%">
Sets the UDF revision level of the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-calculatediscidentifier">CalculateDiscIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves a string that identifies a disc and the sessions recorded on the disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem">CreateDirectoryItem</a>
</td>
<td align="left" width="63%">
Create a directory item with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem">CreateFileItem</a>
</td>
<td align="left" width="63%">
Create a file item with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage">CreateResultImage</a>
</td>
<td align="left" width="63%">
Create the result object that contains the file system and file data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-exists">Exists</a>
</td>
<td align="left" width="63%">
Checks for the existence of a given file or directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_bootimageoptions">get_BootImageOptions</a>
</td>
<td align="left" width="63%">
Retrieves the boot image that you want to add to the file-system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_changepoint">get_ChangePoint</a>
</td>
<td align="left" width="63%">
Retrieves the change point identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_directorycount">get_DirectoryCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of directories in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_filecount">get_FileCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of files in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_filesystemssupported">get_FileSystemsSupported</a>
</td>
<td align="left" width="63%">
Retrieves the list of file system types that a client can use to build a file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_filesystemstocreate">get_FileSystemsToCreate</a>
</td>
<td align="left" width="63%">
Retrieves the types of file systems to create when generating the result stream.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_freemediablocks">get_FreeMediaBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of blocks available for the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_importedvolumename">get_ImportedVolumeName</a>
</td>
<td align="left" width="63%">
Retrieves the volume name provided from an imported file system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root">get_Root</a>
</td>
<td align="left" width="63%">
Retrieves the root directory item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_sessionstartblock">get_SessionStartBlock</a>
</td>
<td align="left" width="63%">
Retrieves the starting block address for the recording session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_strictfilesystemcompliance">get_StrictFileSystemCompliance</a>
</td>
<td align="left" width="63%">
Determines the compliance level for creating and developing the file-system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_udfrevisionssupported">get_UDFRevisionsSupported</a>
</td>
<td align="left" width="63%">
Retrieves a list of supported UDF revision levels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_usedblocks">get_UsedBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the number of blocks in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_userestrictedcharacterset">get_UseRestrictedCharacterSet</a>
</td>
<td align="left" width="63%">
Determines if file and directory names should be restricted to using only CP_ANSI characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumename">get_VolumeName</a>
</td>
<td align="left" width="63%">
Retrieves the volume name for this file system image. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumenameiso9660">get_VolumeNameISO9660</a>
</td>
<td align="left" width="63%">
Retrieves the volume name for the ISO9660 system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumenamejoliet">get_VolumeNameJoliet</a>
</td>
<td align="left" width="63%">
Retrieves the volume name for the Joliet system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_volumenameudf">get_VolumeNameUDF</a>
</td>
<td align="left" width="63%">
Retrieves the volume name for the UDF system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_workingdirectory">get_WorkingDirectory</a>
</td>
<td align="left" width="63%">
Retrieves the temporary directory in which stash files are built.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-getdefaultfilesystemforimport">GetDefaultFileSystemForImport</a>
</td>
<td align="left" width="63%">
Retrieves the file system to import by default.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc">IdentifyFileSystemsOnDisc</a>
</td>
<td align="left" width="63%">
Retrieves a list of the different types of file systems on the optical media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem">ImportFileSystem</a>
</td>
<td align="left" width="63%">
Imports the default file system on the current disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem">ImportSpecificFileSystem</a>
</td>
<td align="left" width="63%">
Import a specific file system from disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-lockinchangepoint">LockInChangePoint</a>
</td>
<td align="left" width="63%">
Locks the file system information at the current change-point level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions">put_BootImageOptions</a>
</td>
<td align="left" width="63%">
Sets the boot image that you want to add to the file-system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_filesystemstocreate">put_FileSystemsToCreate</a>
</td>
<td align="left" width="63%">
Sets the file systems to create when generating the result stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_freemediablocks">put_FreeMediaBlocks</a>
</td>
<td align="left" width="63%">
Sets the maximum number of blocks available for the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_sessionstartblock">put_SessionStartBlock</a>
</td>
<td align="left" width="63%">
Sets the starting block address for the recording session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_stagefiles">put_StageFiles</a>
</td>
<td align="left" width="63%">
Determines if the file system should be staged before the burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_strictfilesystemcompliance">put_StrictFileSystemCompliance</a>
</td>
<td align="left" width="63%">
Determines the compliance level for creating and developing the file-system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_userestrictedcharacterset">put_UseRestrictedCharacterSet</a>
</td>
<td align="left" width="63%">
Determines if file and directory names should be restricted to using only CP_ANSI characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_volumename">put_VolumeName</a>
</td>
<td align="left" width="63%">
Sets the volume name for this file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_workingdirectory">put_WorkingDirectory</a>
</td>
<td align="left" width="63%">
Sets the temporary directory in which stash files are built.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-rollbacktochangepoint">RollbackToChangePoint</a>
</td>
<td align="left" width="63%">
Reverts the image back to the specified change point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-setmaxmediablocksfromdevice">SetMaxMediaBlocksFromDevice</a>
</td>
<td align="left" width="63%">
Set maximum number of blocks available based on the capabilities of the recorder.

</td>
</tr>
</table> 


## -remarks



To create the <b>CFileSystemImage</b> object in a script, use IMAPI2.MsftFileSystemImage as the program identifier when calling <b>CreateObject</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents">DFileSystemImageEvents</a>
 

 


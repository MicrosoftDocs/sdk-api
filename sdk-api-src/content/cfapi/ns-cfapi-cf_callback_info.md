---
UID: NS:cfapi.CF_CALLBACK_INFO
title: CF_CALLBACK_INFO
author: windows-sdk-content
description: Contains common callback information.
old-location: cloudapi\cf_callback_info.htm
old-project: cfApi
ms.assetid: EF24E61E-4AF7-4946-A326-1F045267AE01
ms.author: windowssdkdev
ms.date: 02/27/2018
ms.keywords: CF_CALLBACK_INFO, CF_CALLBACK_INFO structure, cfapi/CF_CALLBACK_INFO, cloudApi.cf_callback_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: cfapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CF_CALLBACK_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CALLBACK_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CF_CALLBACK_INFO structure


## -description


Contains common callback information.


## -struct-fields




### -field StructSize

The size of the structure.


### -field ConnectionKey

An opaque handle created by <a href="https://msdn.microsoft.com/287DA978-9797-48DF-9C90-BA53BB82475C">CfConnectSyncRoot</a> for a sync root managed by the sync provider. 


### -field CallbackContext

points to an opaque blob that the sync provider provides at the sync root connect time. 


### -field VolumeGuidName

GUID name of the volume on which the placeholder file/directory to be serviced resides. It is in the form: “\\?\Volume{GUID}”.


### -field VolumeDosName

DOS drive letter of the volume in the form of “X:” where X is the drive letter.


### -field VolumeSerialNumber

The serial number of the volume.


### -field SyncRootFileId

A 64 bit file system maintained volume-wide unique ID of the sync root under which the placeholder file/directory to be serviced resides.


### -field SyncRootIdentity

Points to the opaque blob provided by the  sync provider at the sync root registration time.


### -field SyncRootIdentityLength

The length, in bytes, of the <b>SyncRootIdentity</b>.


### -field FileId

A 64 bit file system maintained, volume-wide unique ID of the placeholder file/directory to be serviced.


### -field FileSize

The logical size of the placeholder file to be serviced. It is always 0 if the subject of the callback is a directory.


### -field FileIdentity

Points to the opaque blob that the sync provider provides at the placeholder creation/conversion/update time.


### -field FileIdentityLength

The length, in bytes, of <b>FileIdentity</b>.


### -field NormalizedPath

The absolute path of the placeholder file/directory to be serviced on the volume identified by VolumeGuidName/VolumeDosName. It starts from the root directory of the volume. See the Remarks section for more details.


### -field TransferKey

An opaque handle to the placeholder file/directory to be serviced. The sync provider must pass it back to the <a href="https://msdn.microsoft.com/6AC8958D-B060-4468-9811-9BAB0E6A06D3">CfExecute</a> call in order to perform the desired operation on the file/directory.


### -field PriorityHint

A numeric scale given to the sync provider to describe the relative priority of one fetch compared to another fetch, in order to provide the most responsive experience to the user.  The values range from 0 (lowest possible priority) to 15 (highest possible priority).


### -field CorrelationVector

An optional correlation vector.


### -field ProcessInfo

Points to a structure that contains the information about the user process that triggers this callback.


### -field RequestKey

 




#### - CommandLine

<div class="alert"><b>Note</b>  This member is new for Windows 10, version 1803.</div>
<div> </div>
The string that is used to start the process. If the platform failed to retrieve the command line, “UNKNOWN” will be returned. 



#### - SessionId

<div class="alert"><b>Note</b>  This member is new for Windows 10, version 1803.</div>
<div> </div>
The 32bit ID of the session wherein the user process that triggers the callback resides. 



## -remarks




A file name is considered normalized if all of the following are true:

<ul>
<li>It contains the full directory path for the file, including the volume name, unless the user opened the file by file ID but does not have traverse privilege for the entire path. (For more information, see <a href="https://msdn.microsoft.com/707e7e83-31d8-46cf-a2ef-e53a20edaeff">FltGetFileNameInformation</a>.)
</li>
<li>The volume name is the volume's non-persistent device object name (for example, "\Device\HarddiskVolume1").
</li>
<li>All short names are expanded to the equivalent long names.
</li>
<li>Any trailing ":$DATA" or "::$DATA" strings are removed from the stream name.
</li>
<li>	All mount points are resolved.
</li>
</ul>





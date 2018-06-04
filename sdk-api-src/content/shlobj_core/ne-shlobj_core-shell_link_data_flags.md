---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SHELL_LINK_DATA_FLAGS enumeration


## -description


Specifies option settings. Used with <a href="https://msdn.microsoft.com/d6ebfd84-6ef4-43be-af16-71fc395c4735">IShellLinkDataList::GetFlags</a> and <a href="https://msdn.microsoft.com/0fca6394-e8ad-4ef3-a7d8-60e85229556b">IShellLinkDataList::SetFlags</a>.


## -enum-fields




### -field SLDF_DEFAULT

0x00000000. Default value used when no other flag is explicitly set.


### -field SLDF_HAS_ID_LIST

0x00000001. The Shell link was saved with an ID list.


### -field SLDF_HAS_LINK_INFO

0x00000002. The Shell link was saved with link information to enable distributed tracking. This information is used by .lnk files to locate the target if the targets's path has changed. It includes information such as volume label and serial number, although the specific stored information can change from release to release.


### -field SLDF_HAS_NAME

0x00000004. The link has a name.


### -field SLDF_HAS_RELPATH

0x00000008. The link has a relative path.


### -field SLDF_HAS_WORKINGDIR

0x00000010. The link has a working directory.


### -field SLDF_HAS_ARGS

0x00000020. The link has arguments.


### -field SLDF_HAS_ICONLOCATION

0x00000040. The link has an icon location.


### -field SLDF_UNICODE

0x00000080. Stored strings are Unicode.


### -field SLDF_FORCE_NO_LINKINFO

0x00000100. Prevents the storage of link tracking information. If this flag is set, it is less likely, though not impossible, that a target can be found by the link if that target is moved.


### -field SLDF_HAS_EXP_SZ

0x00000200. The link contains expandable environment strings such as <code>%windir%</code>.


### -field SLDF_RUN_IN_SEPARATE

0x00000400. Causes a 16-bit target application to run in a separate Virtual DOS Machine (VDM)/Windows on Windows (WOW).


### -field SLDF_HAS_LOGO3ID

0x00000800. Not supported. Note that as of Windows Vista, this value is no longer defined.


### -field SLDF_HAS_DARWINID

0x00001000. The link is a special Windows Installer link.


### -field SLDF_RUNAS_USER

0x00002000. Causes the target application to run as a different user.


### -field SLDF_HAS_EXP_ICON_SZ

0x00004000. The icon path in the link contains an expandable environment string such as such as <code>%windir%</code>.


### -field SLDF_NO_PIDL_ALIAS

0x00008000. Prevents the use of ID list alias mapping when parsing the ID list from the path.


### -field SLDF_FORCE_UNCNAME

0x00010000. Forces the use of the UNC name (a full network resource name), rather than the local name.


### -field SLDF_RUN_WITH_SHIMLAYER

0x00020000. Causes the target of this link to launch with a shim layer active. A shim is an intermediate DLL that facilitates compatibility between otherwise incompatible software services. Shims are typically used to provide version compatibility.


### -field SLDF_FORCE_NO_LINKTRACK

0x00040000. <b>Introduced in Windows Vista</b>. Disable object ID distributed tracking information.


### -field SLDF_ENABLE_TARGET_METADATA

0x00080000. <b>Introduced in Windows Vista</b>. Enable the caching of target metadata into the link file.


### -field SLDF_DISABLE_LINK_PATH_TRACKING

0x00100000. <b>Introduced in Windows 7</b>. Disable shell link tracking.


### -field SLDF_DISABLE_KNOWNFOLDER_RELATIVE_TRACKING

0x00200000. <b>Introduced in Windows Vista</b>. Disable known folder tracking information.


### -field SLDF_NO_KF_ALIAS

0x00400000. <b>Introduced in Windows 7</b>. Disable known folder alias mapping when loading the IDList during deserialization.


### -field SLDF_ALLOW_LINK_TO_LINK

0x00800000. <b>Introduced in Windows 7</b>. Allow link to point to another shell link as long as this does not create cycles. 


### -field SLDF_UNALIAS_ON_SAVE

0x01000000. <b>Introduced in Windows 7</b>. Remove alias when saving the IDList.


### -field SLDF_PREFER_ENVIRONMENT_PATH

0x02000000. <b>Introduced in Windows 7</b>. Recalculate the IDList from the path with the environmental variables at load time, rather than persisting the IDList. 


### -field SLDF_KEEP_LOCAL_IDLIST_FOR_UNC_TARGET

0x04000000. <b>Introduced in Windows 7</b>. If the target is a UNC location on a local machine, keep the local IDList target in addition to the remote target. 


### -field SLDF_PERSIST_VOLUME_ID_RELATIVE

0x08000000. <b>Introduced in Windows 8</b>. Persist the target IDlist in its volume-ID-relative form to avoid a dependency on drive letters.


### -field SLDF_VALID

<b>Introduced in Windows Vista</b>. A mask for valid <a href="https://msdn.microsoft.com/3b810223-b2d9-40ca-92bd-4d9f31981355">SHELL_LINK_DATA_FLAGS</a> bits.

                        

<table class="clsStd">
<tr>
<th>OS</th>
<th>Value</th>
</tr>
<tr>
<td>Windows 8</td>
<td>0x0FFFF7FF</td>
</tr>
<tr>
<td>Windows 7</td>
<td>0x07FFF7FF</td>
</tr>
<tr>
<td>Windows Vista</td>
<td>0x003FF7FF</td>
</tr>
</table>
 


### -field SLDF_RESERVED

Reserved; do not use.


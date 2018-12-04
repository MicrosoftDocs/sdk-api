---
UID: NE:shlobj_core.__unnamed_enum_7
title: SHARD
author: windows-sdk-content
description: Indicates the interpretation of the data passed by SHAddToRecentDocs in its pv parameter to identify the item whose usage statistics are being tracked.
old-location: shell\SHARD.htm
tech.root: shell
ms.assetid: efc9e018-41bb-44ef-9ca8-85d9e34c9899
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: SHARD, SHARD enumeration [Windows Shell], SHARD_APPIDINFO, SHARD_APPIDINFOIDLIST, SHARD_APPIDINFOLINK, SHARD_LINK, SHARD_PATHA, SHARD_PATHW, SHARD_PIDL, SHARD_SHELLITEM, _shell_SHARD, shell.SHARD, shlobj_core/SHARD, shlobj_core/SHARD_APPIDINFO, shlobj_core/SHARD_APPIDINFOIDLIST, shlobj_core/SHARD_APPIDINFOLINK, shlobj_core/SHARD_LINK, shlobj_core/SHARD_PATHA, shlobj_core/SHARD_PATHW, shlobj_core/SHARD_PIDL, shlobj_core/SHARD_SHELLITEM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SHARD
product: Windows
targetos: Windows
req.typenames: SHARD
req.redist: 
---

# SHARD enumeration


## -description


Indicates the interpretation of the data passed by <a href="https://msdn.microsoft.com/84e065e6-b68d-4303-b98b-3f8507539468">SHAddToRecentDocs</a> in its <i>pv</i> parameter to identify the item whose usage statistics are being tracked.


## -enum-fields




### -field SHARD_PIDL

The <i>pv</i> parameter points to a PIDL that identifies the document's file object. PIDLs that identify non-file objects are not accepted.


### -field SHARD_PATHA

The <i>pv</i> parameter points to a null-terminated ANSI string with the path and file name of the object.


### -field SHARD_PATHW

The <i>pv</i> parameter points to a null-terminated Unicode string with the path and file name of the object.


### -field SHARD_APPIDINFO

<b>Windows 7 and later</b>. The <i>pv</i> parameter points to a <a href="https://msdn.microsoft.com/bb2b7e86-04ca-4dd0-944b-a95e8a0be1e0">SHARDAPPIDINFO</a> structure that pairs an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that identifies the item with an AppUserModelID that associates it with a particular process or application.


### -field SHARD_APPIDINFOIDLIST

<b>Windows 7 and later</b>. The <i>pv</i> parameter points to a <a href="https://msdn.microsoft.com/11c69ff9-b8a0-4168-8036-f45a9f7813ba">SHARDAPPIDINFOIDLIST</a> structure that pairs an absolute PIDL that identifies the item with an AppUserModelID that associates it with a particular process or application.


### -field SHARD_LINK

<b>Windows 7 and later</b>. The <i>pv</i> parameter is an interface pointer to an <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> object.


### -field SHARD_APPIDINFOLINK

<b>Windows 7 and later</b>. The <i>pv</i> parameter points to a <a href="https://msdn.microsoft.com/01613dc9-4516-4995-bd31-feee2eb650b2">SHARDAPPIDINFOLINK</a> structure that pairs an <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> that identifies the item with an AppUserModelID that associates it with a particular process or application.


### -field SHARD_SHELLITEM

<b>Windows 7 and later</b>. The <i>pv</i> parameter is an interface pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object.


## -remarks



Before Windows 7, SHARD_PIDL, SHARD_PATHA, and SHARD_PATHW were defined as individual constants, not as enumeration members.

When providing an <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> through either <b><b>SHARD_LINK</b></b> or <b><b>SHARD_APPIDINFOLINK</b></b>, the <b>IShellLink</b> instance must provide the following:

                

<ul>
<li>Either a PIDL (<a href="https://msdn.microsoft.com/4c0571a5-1615-4c3f-b9a6-0667df07165b">IShellLink::SetIDList</a>) or the target path (<a href="https://msdn.microsoft.com/032610ba-d6ff-4200-8fd3-455460587dec">IShellLink::SetPath</a> or <a href="https://msdn.microsoft.com/f9cbd1db-253b-4ce8-a8ea-cfc48759c9d3">IShellLink::SetRelativePath</a>)</li>
<li>Command-line arguments (<a href="https://msdn.microsoft.com/5ad5fabd-be12-40bc-a6b3-498bcde7223a">IShellLink::SetArguments</a>)</li>
<li>Icon location  (<a href="https://msdn.microsoft.com/1ba267f2-ae05-4a6d-be3c-382a89e17d92">IShellLink::SetIconLocation</a>)</li>
</ul>
The display name must be set through the item's <a href="https://msdn.microsoft.com/8fb948d6-2677-4e5d-b283-8757c3df574d">System.Title (PKEY_Title)</a> property. The property can directly hold the display name or it can be an indirect string representation, such as "@shell32.dll,-1324", to use a stored string. An indirect string enables the item name to be displayed in the user's selected language.

Optionally, the description field (<a href="https://msdn.microsoft.com/4bec482e-04e6-4cde-ab8e-23c5a1463bdf">IShellLink::SetDescription</a>) can be set to provide a custom tooltip for the item in the Jump List.




## -see-also




<a href="https://msdn.microsoft.com/84e065e6-b68d-4303-b98b-3f8507539468">SHAddToRecentDocs</a>
 

 


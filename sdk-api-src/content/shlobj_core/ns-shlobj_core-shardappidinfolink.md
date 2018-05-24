---
UID: NS:shlobj_core.SHARDAPPIDINFOLINK
title: SHARDAPPIDINFOLINK
author: windows-driver-content
description: Contains data used by SHAddToRecentDocs to identify both an item, in this case through an IShellLink, and the process that it is associated with.
old-location: shell\SHARDAPPIDINFOLINK.htm
old-project: shell
ms.assetid: 01613dc9-4516-4995-bd31-feee2eb650b2
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: SHARDAPPIDINFOLINK, SHARDAPPIDINFOLINK structure [Windows Shell], _shell_SHARDAPPIDINFOLINK, shell.SHARDAPPIDINFOLINK, shlobj_core/SHARDAPPIDINFOLINK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SHARDAPPIDINFOLINK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shlobj_core.h
api_name:
-	SHARDAPPIDINFOLINK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# SHARDAPPIDINFOLINK structure


## -description


Contains data used by <a href="https://msdn.microsoft.com/84e065e6-b68d-4303-b98b-3f8507539468">SHAddToRecentDocs</a> to identify both an item, in this case through an <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a>, and the process that it is associated with.


## -struct-fields




### -field psl

Type: <b><a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> instance that, when launched, opens the item. The shortcut is not added by <a href="https://msdn.microsoft.com/84e065e6-b68d-4303-b98b-3f8507539468">SHAddToRecentDocs</a> to the user's <b>Recent</b> folder (<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL_RECENT</a>, <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">FOLDERID_Recent</a>), but it is added to the <b>Recent</b> category in the specified application's Jump List.


### -field pszAppID

Type: <b>PCWSTR</b>

The application-defined AppUserModelID associated with the item.


## -remarks



The <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> instance pointed to by <b>psl</b> must provide the following:

                

<ul>
<li>Either a pointer to an item identifier list (PIDL) (<a href="https://msdn.microsoft.com/4c0571a5-1615-4c3f-b9a6-0667df07165b">IShellLink::SetIDList</a>) or the target path (<a href="https://msdn.microsoft.com/032610ba-d6ff-4200-8fd3-455460587dec">IShellLink::SetPath</a> or <a href="https://msdn.microsoft.com/f9cbd1db-253b-4ce8-a8ea-cfc48759c9d3">IShellLink::SetRelativePath</a>)</li>
<li>Command-line arguments (<a href="https://msdn.microsoft.com/5ad5fabd-be12-40bc-a6b3-498bcde7223a">IShellLink::SetArguments</a>)</li>
<li>Icon location  (<a href="https://msdn.microsoft.com/1ba267f2-ae05-4a6d-be3c-382a89e17d92">IShellLink::SetIconLocation</a>)</li>
</ul>
The display name must be set through the item's <a href="https://msdn.microsoft.com/8fb948d6-2677-4e5d-b283-8757c3df574d">System.Title (PKEY_Title)</a> property. The property can directly hold the display name or it can be an indirect string representation, such as "@shell32.dll,-1324", to use a stored string. An indirect string enables the item name to be displayed in the user's selected language.

Optionally, the description field (<a href="https://msdn.microsoft.com/4bec482e-04e6-4cde-ab8e-23c5a1463bdf">IShellLink::SetDescription</a>) can be set to provide a custom tooltip for the item in the Jump List.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://msdn.microsoft.com/bb2b7e86-04ca-4dd0-944b-a95e8a0be1e0">SHARDAPPIDINFO</a>



<a href="https://msdn.microsoft.com/11c69ff9-b8a0-4168-8036-f45a9f7813ba">SHARDAPPIDINFOIDLIST</a>



<a href="https://msdn.microsoft.com/84e065e6-b68d-4303-b98b-3f8507539468">SHAddToRecentDocs</a>
 

 


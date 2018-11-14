---
UID: NS:tspubplugin2com.__MIDL_ItsPubPlugin2_0001
title: "__MIDL_ItsPubPlugin2_0001"
author: windows-sdk-content
description: Contains information about a file association in RemoteApp and Desktop Connection.
old-location: termserv\pluginresource2fileassociation.htm
tech.root: termserv
ms.assetid: A3485D5F-EBF0-480B-9AD2-534361E82B40
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "__MIDL_ItsPubPlugin2_0001, pluginResource2FileAssociation, pluginResource2FileAssociation structure [Remote Desktop Services], termserv.pluginresource2fileassociation, tspubplugin2com/pluginResource2FileAssociation"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tspubplugin2com.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tspubplugin2com.idl
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
 - tspubplugin2com.h
api_name:
 - pluginResource2FileAssociation
product: Windows
targetos: Windows
req.typenames: pluginResource2FileAssociation
req.redist: 
---

# __MIDL_ItsPubPlugin2_0001 structure


## -description


Contains information about a file association in RemoteApp and Desktop Connection.


## -struct-fields




### -field extName

A null-terminated string that contains the file name extension. The length of this string is limited to <b>MAX_FILE_ASSOC_EXTENSION_SIZE</b> characters, including the terminating <b>NULL</b> character.


### -field primaryHandler

Indicates if this is the primary handler for the file association.


### -field pceIconSize

The size, in bytes, of the <b>iconContents</b> buffer.


### -field iconContents

A byte array that contains the icon to display for files with the specified extension.


## -remarks



<b>MAX_FILE_ASSOC_EXTENSION_SIZE</b> is declared as follows:

<code>#define MAX_FILE_ASSOC_EXTENSION_SIZE 256</code>




## -see-also




<a href="https://msdn.microsoft.com/BD4761C7-377C-499C-B984-3B126C704089">pluginResource2</a>
 

 


---
UID: NF:tspubplugin2com.ItsPubPlugin2.DeletePersonalDesktopAssignment
title: ItsPubPlugin2::DeletePersonalDesktopAssignment (tspubplugin2com.h)
author: windows-sdk-content
description: Called to delete a mapping between the specified user and a virtual machine in a personal virtual desktop collection.
old-location: termserv\itspubplugin2_deletepersonaldesktopassignment.htm
tech.root: TermServ
ms.assetid: 962d7de7-a447-44f9-b3bd-a87d122a6328
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeletePersonalDesktopAssignment, DeletePersonalDesktopAssignment method [Remote Desktop Services], DeletePersonalDesktopAssignment method [Remote Desktop Services],ItsPubPlugin2 interface, ItsPubPlugin2 interface [Remote Desktop Services],DeletePersonalDesktopAssignment method, ItsPubPlugin2.DeletePersonalDesktopAssignment, ItsPubPlugin2::DeletePersonalDesktopAssignment, termserv.itspubplugin2_deletepersonaldesktopassignment, tspubplugin2com/ItsPubPlugin2::DeletePersonalDesktopAssignment
ms.topic: method
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
 - COM
api_location:
 - tspubplugin2com.h
api_name:
 - ItsPubPlugin2.DeletePersonalDesktopAssignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ItsPubPlugin2::DeletePersonalDesktopAssignment


## -description


Called to delete a mapping between the specified user and a virtual machine in a personal virtual desktop collection.


## -parameters




### -param userId [in]

A null-terminated string that contains the security identifier (SID) of the user.


### -param poolId [in]

A null-terminated string that contains the identifier of the collection that the personal desktop exists in.


### -param endpointName [in]

A null-terminated string that contains the name of the desktop end point to be deleted.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1ef27b3a-b897-4757-803d-d3a18959895c">ItsPubPlugin2</a>
 

 


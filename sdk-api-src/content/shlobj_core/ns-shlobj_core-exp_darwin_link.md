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

# EXP_DARWIN_LINK structure


## -description


Holds an extra data block used by <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>. It holds the link's Windows Installer ID.


## -struct-fields




### -field dbh

Type: <b><a href="https://msdn.microsoft.com/06de45c2-8cb5-45e3-9639-d4625c24d27b">DATABLOCK_HEADER</a></b>


<a href="https://msdn.microsoft.com/06de45c2-8cb5-45e3-9639-d4625c24d27b">DATABLOCK_HEADER</a> structure stating the size and signature of the <b>EXP_DARWIN_LINK</b> structure. The following is the only recognized signature value.



#### EXP_DARWIN_ID_SIG

The <b>EXP_DARWIN_LINK</b> structure contains a Windows Installer ID.


### -field DUMMYSTRUCTNAME

 


### -field szDarwinID

Type: <b>__wchar_t[MAX_PATH]</b>

The link's ID in the form of an ANSI string.


### -field szwDarwinID

Type: <b>WCHAR[MAX_PATH]</b>

The link's ID in the form of an Unicode string.


## -remarks




<a href="https://msdn.microsoft.com/d6ebfd84-6ef4-43be-af16-71fc395c4735">IShellLinkDataList::GetFlags</a> returns the flag SLDF_HAS_DARWINID for links that have a darwin signature.




## -see-also




<a href="https://msdn.microsoft.com/d6ebfd84-6ef4-43be-af16-71fc395c4735">IShellLinkDataList::GetFlags</a>
 

 


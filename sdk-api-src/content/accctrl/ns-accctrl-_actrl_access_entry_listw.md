---
UID: NS:accctrl._ACTRL_ACCESS_ENTRY_LISTW
title: "_ACTRL_ACCESS_ENTRY_LISTW"
author: windows-sdk-content
description: Contains a list of access entries.
old-location: com\actrl_access_entry_list.htm
old-project: com
ms.assetid: d0e71756-0247-4c6b-b8b5-a343121b7406
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PACTRL_ACCESS_ENTRY_LISTW, ACTRL_ACCESS_ENTRY_LIST, ACTRL_ACCESS_ENTRY_LIST structure [COM], ACTRL_ACCESS_ENTRY_LISTA, ACTRL_ACCESS_ENTRY_LISTW, PACTRL_ACCESS_ENTRY_LIST, PACTRL_ACCESS_ENTRY_LIST structure pointer [COM], _ACTRL_ACCESS_ENTRY_LISTA, _ACTRL_ACCESS_ENTRY_LISTW, accctrl/ACTRL_ACCESS_ENTRY_LIST, accctrl/ACTRL_ACCESS_ENTRY_LISTA, accctrl/ACTRL_ACCESS_ENTRY_LISTW, accctrl/PACTRL_ACCESS_ENTRY_LIST, com.actrl_access_entry_list"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ACTRL_ACCESS_ENTRY_LISTW (Unicode) and ACTRL_ACCESS_ENTRY_LISTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ACTRL_ACCESS_ENTRY_LISTW, *PACTRL_ACCESS_ENTRY_LISTW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - ACTRL_ACCESS_ENTRY_LIST
 - ACTRL_ACCESS_ENTRY_LISTA
 - ACTRL_ACCESS_ENTRY_LISTW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
---

# _ACTRL_ACCESS_ENTRY_LISTW structure


## -description


Contains a list of access entries.


## -struct-fields




### -field cEntries

The number of entries in the <b>pAccessList</b> array.


### -field pAccessList

A pointer to an array of <a href="https://msdn.microsoft.com/bcb2ad72-7b00-4582-b05e-e00720a4db77">ACTRL_ACCESS_ENTRY</a> structures. Each structure specifies access-control information for a specified trustee. 



### -field pAccessList.size_is

 


### -field pAccessList.size_is.cEntries

 




## -remarks



To create an empty access list, set <b>cEntries</b> to zero and <b>pAccessList</b> to <b>NULL</b>. An empty list does not grant access to any trustee, and thus, denies all access to an object.

To create a null access list, set the <b>pAccessEntryList</b> member of the <a href="https://msdn.microsoft.com/90b13dd1-0ca6-4674-b9fa-a61aed4637d7">ACTRL_PROPERTY_ENTRY</a> structure to <b>NULL</b>. A null access list grants everyone full access to the object.




## -see-also




<a href="https://msdn.microsoft.com/90b13dd1-0ca6-4674-b9fa-a61aed4637d7">ACTRL_PROPERTY_ENTRY</a>
 

 


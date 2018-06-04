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

# _WSB_OB_STATUS_ENTRY structure


## -description


 The <b>WSB_OB_STATUS_ENTRY</b> structure contains status 
    information for one entry to be shown in the Windows Server Backup MMC snap-in.


## -struct-fields




### -field m_dwIcon

The resource identifier of the icon to be shown with the status entry. A value of zero indicates no icon is 
      to be shown.


### -field m_dwStatusEntryName

The resource identifier of the name of the status entry.


### -field m_dwStatusEntryValue

The resource identifier of the value of the status entry.


### -field m_cValueTypePair

The number of 
      <a href="https://msdn.microsoft.com/FA92796E-7C26-4FD0-8AC2-F84F8F5E5A6C">WSB_OB_STATUS_ENTRY_VALUE_TYPE_PAIR</a> 
      structures pointed to by the <b>m_rgValueTypePair</b> member.


### -field m_rgValueTypePair

The list of parameters used to expand the value string contained in the 
      <b>m_dwStatusEntryValue</b> member.


## -remarks



The resources indicated by the resource IDs contained in the <b>m_dwIcon</b>, 
      <b>m_dwStatusEntryName</b> and <b>m_dwStatusEntryValue</b> members will 
      be loaded from the same DLL provided by the cloud backup provider during its registration with Windows Server 
      Backup. For example, an entry name resource ID could point to the string "Total Backups:" or an 
      entry value resource ID could point to the string "%0 copies".




## -see-also




<a href="https://msdn.microsoft.com/C1AC87C6-37B7-4675-AB51-45C292239EB5">Cloud  Backup Provider API Structures</a>



<a href="https://msdn.microsoft.com/FA92796E-7C26-4FD0-8AC2-F84F8F5E5A6C">WSB_OB_STATUS_ENTRY_VALUE_TYPE_PAIR</a>
 

 


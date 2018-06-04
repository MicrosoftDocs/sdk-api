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

# _FH_LOCAL_POLICY_TYPE enumeration


## -description


Specifies the type of a local policy for the File History feature. Each local policy has a numeric parameter associated with it.


## -enum-fields




### -field FH_FREQUENCY

This local policy specifies how frequently backups are to be performed for the current user. The numeric parameter contains the time, in seconds, from the end of one backup until the start of the next one. The default value of the numeric parameter for this policy is 3600 seconds (1 hour).


### -field FH_RETENTION_TYPE

This  local policy specifies when previous versions of files and folders can be deleted from a backup target. See the <a href="https://msdn.microsoft.com/B80EC7BF-1825-462C-ACE3-5163C14EE15D">FH_RETENTION_TYPES</a> enumeration for the list of possible values. The default value of the numeric parameter for this policy is <b>FH_RETENTION_DISABLED</b>.


### -field FH_RETENTION_AGE

This local policy specifies the minimum age of previous versions that can be deleted from a backup target when the  <b>FH_RETENTION_AGE_BASED</b> retention type is specified. For more information, see the <a href="https://msdn.microsoft.com/B80EC7BF-1825-462C-ACE3-5163C14EE15D">FH_RETENTION_TYPES</a> enumeration. The numeric parameter contains the minimum age, in days. The default value of the numeric parameter for this policy is 365 days (1 year).


### -field MAX_LOCAL_POLICY

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.


## -remarks



To retrieve the value of the numeric parameter for a local policy, use the <a href="https://msdn.microsoft.com/380B77C3-CA93-48D6-9915-FB788CF24C99">IFhConfigMgr::GetLocalPolicy</a> method.

To set the value of the numeric parameter for the local policy, use the <a href="https://msdn.microsoft.com/A1106349-6B14-4A44-B845-7853FA1919D6">IFhConfigMgr::SetLocalPolicy</a> method.




## -see-also




<a href="https://msdn.microsoft.com/B80EC7BF-1825-462C-ACE3-5163C14EE15D">FH_RETENTION_TYPES</a>



<a href="https://msdn.microsoft.com/380B77C3-CA93-48D6-9915-FB788CF24C99">IFhConfigMgr::GetLocalPolicy</a>



<a href="https://msdn.microsoft.com/A1106349-6B14-4A44-B845-7853FA1919D6">IFhConfigMgr::SetLocalPolicy</a>
 

 


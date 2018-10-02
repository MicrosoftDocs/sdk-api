---
UID: NE:fhcfg._FH_LOCAL_POLICY_TYPE
title: "_FH_LOCAL_POLICY_TYPE"
author: windows-sdk-content
description: Specifies the type of a local policy for the File History feature. Each local policy has a numeric parameter associated with it.
old-location: winprog\fh_local_policy_type.htm
tech.root: devnotes
ms.assetid: 59C54A67-91A3-495F-95F2-50EB373D442C
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*PFH_LOCAL_POLICY_TYPE, FH_FREQUENCY, FH_LOCAL_POLICY_TYPE, FH_LOCAL_POLICY_TYPE enumeration [Windows API], FH_RETENTION_AGE, FH_RETENTION_TYPE, MAX_LOCAL_POLICY, _FH_LOCAL_POLICY_TYPE, fhcfg/FH_FREQUENCY, fhcfg/FH_LOCAL_POLICY_TYPE, fhcfg/FH_RETENTION_AGE, fhcfg/FH_RETENTION_TYPE, fhcfg/MAX_LOCAL_POLICY, winprog.fh_local_policy_type"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - Fhcfg.h
api_name:
 - FH_LOCAL_POLICY_TYPE
product: Windows
targetos: Windows
req.typenames: FH_LOCAL_POLICY_TYPE, *PFH_LOCAL_POLICY_TYPE
req.redist: 
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
 

 


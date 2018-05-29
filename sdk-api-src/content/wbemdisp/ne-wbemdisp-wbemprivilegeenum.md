---
UID: NE:wbemdisp.WbemPrivilegeEnum
title: WbemPrivilegeEnum
author: windows-sdk-content
description: Define privileges. These constants are used with SWbemSecurity to grant the privileges required for some operations.
old-location: wmi\wbemprivilegeenum.htm
old-project: WmiSdk
ms.assetid: 235a1115-d8c4-4334-a4e0-fc539da4d2ae
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: WbemPrivilegeEnum, WbemPrivilegeEnum enumeration [Windows Management Instrumentation], wbemPrivilegeAudit, wbemPrivilegeBackup, wbemPrivilegeChangeNotify, wbemPrivilegeCreatePagefile, wbemPrivilegeCreatePermanent, wbemPrivilegeCreateToken, wbemPrivilegeDebug, wbemPrivilegeEnableDelegation, wbemPrivilegeIncreaseBasePriority, wbemPrivilegeIncreaseQuota, wbemPrivilegeLoadDriver, wbemPrivilegeLockMemory, wbemPrivilegeMachineAccount, wbemPrivilegeManageVolume, wbemPrivilegePrimaryToken, wbemPrivilegeProfileSingleProcess, wbemPrivilegeRemoteShutdown, wbemPrivilegeRestore, wbemPrivilegeSecurity, wbemPrivilegeShutdown, wbemPrivilegeSyncAgent, wbemPrivilegeSystemEnvironment, wbemPrivilegeSystemProfile, wbemPrivilegeSystemtime, wbemPrivilegeTakeOwnership, wbemPrivilegeTcb, wbemPrivilegeUndock, wbemdisp/WbemPrivilegeEnum, wbemdisp/wbemPrivilegeAudit, wbemdisp/wbemPrivilegeBackup, wbemdisp/wbemPrivilegeChangeNotify, wbemdisp/wbemPrivilegeCreatePagefile, wbemdisp/wbemPrivilegeCreatePermanent, wbemdisp/wbemPrivilegeCreateToken, wbemdisp/wbemPrivilegeDebug, wbemdisp/wbemPrivilegeEnableDelegation, wbemdisp/wbemPrivilegeIncreaseBasePriority, wbemdisp/wbemPrivilegeIncreaseQuota, wbemdisp/wbemPrivilegeLoadDriver, wbemdisp/wbemPrivilegeLockMemory, wbemdisp/wbemPrivilegeMachineAccount, wbemdisp/wbemPrivilegeManageVolume, wbemdisp/wbemPrivilegePrimaryToken, wbemdisp/wbemPrivilegeProfileSingleProcess, wbemdisp/wbemPrivilegeRemoteShutdown, wbemdisp/wbemPrivilegeRestore, wbemdisp/wbemPrivilegeSecurity, wbemdisp/wbemPrivilegeShutdown, wbemdisp/wbemPrivilegeSyncAgent, wbemdisp/wbemPrivilegeSystemEnvironment, wbemdisp/wbemPrivilegeSystemProfile, wbemdisp/wbemPrivilegeSystemtime, wbemdisp/wbemPrivilegeTakeOwnership, wbemdisp/wbemPrivilegeTcb, wbemdisp/wbemPrivilegeUndock, wmi.wbemprivilegeenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WbemPrivilegeEnum
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wbemdisp.h
api_name:
-	WbemPrivilegeEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WbemPrivilegeEnum enumeration


## -description


The 
WbemPrivilegeEnum constants define privileges. These constants are used with 
<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a> to grant the privileges required for some operations. For more information, see 
<a href="https://msdn.microsoft.com/f9400597-81bb-44a8-80dc-aba0160aea26">Privilege Constants</a>.

The WMI scripting type library, wbemdisp.tlb defines these constants. Microsoft Visual Basic applications can access this library; script languages must use the value of the constant directly, unless they use Windows Script Host (WSH) XML file format. For more information, see 
<a href="https://msdn.microsoft.com/6ef4e210-0733-4f2a-89c1-1a7aca5a19d9">Using the WMI Scripting Type Library</a>.


## -enum-fields




### -field wbemPrivilegeCreateToken

Required to create a primary token.


### -field wbemPrivilegePrimaryToken

Required to assign the primary token of a process.


### -field wbemPrivilegeLockMemory

Required to lock physical pages in memory.


### -field wbemPrivilegeIncreaseQuota

Required to increase the quota assigned to a process.


### -field wbemPrivilegeMachineAccount

Required to create a machine account.


### -field wbemPrivilegeTcb

Identifies its holder as part of the trusted computer base. Some trusted, protected subsystems are granted this privilege.


### -field wbemPrivilegeSecurity

Required to perform a number of security-related functions, such as controlling and viewing audit messages. This privilege identifies its holder as a security operator.


### -field wbemPrivilegeTakeOwnership

Required to take ownership of an object without being granted discretionary access. This privilege allows the owner value to be set only to those values that the holder may legitimately assign as the owner of an object.


### -field wbemPrivilegeLoadDriver

Required to load or unload a device driver.


### -field wbemPrivilegeSystemProfile

Required to gather profiling information for the entire system.


### -field wbemPrivilegeSystemtime

Required to modify the system time.


### -field wbemPrivilegeProfileSingleProcess

Required to gather profiling information for a single process.


### -field wbemPrivilegeIncreaseBasePriority

Required to increase the base priority of a process.


### -field wbemPrivilegeCreatePagefile

Required to create a paging file.


### -field wbemPrivilegeCreatePermanent

Required to create a permanent object.


### -field wbemPrivilegeBackup

Required to perform backup operations.


### -field wbemPrivilegeRestore

Required to perform restore operations. This privilege enables you to set any valid user or group security identifier (SID)  as the owner of an object.


### -field wbemPrivilegeShutdown

Required to shut down a local system.


### -field wbemPrivilegeDebug

Required to debug a process.


### -field wbemPrivilegeAudit

Required to generate audit-log entries.


### -field wbemPrivilegeSystemEnvironment

Required to modify the nonvolatile RAM of systems that use this type of memory to store configuration information.


### -field wbemPrivilegeChangeNotify

Required to receive notifications of changes to files or directories. This privilege also causes the system to skip all traversal access checks. It is enabled by default for all users.


### -field wbemPrivilegeRemoteShutdown

Required to shut down a system using a network request.


### -field wbemPrivilegeUndock

Required to remove a computer from a docking station.


### -field wbemPrivilegeSyncAgent

Required to synchronize directory service data.


### -field wbemPrivilegeEnableDelegation

Required to enable computer and user accounts to be trusted for delegation.


### -field wbemPrivilegeManageVolume

Required to perform volume maintenance tasks.


## -see-also




<a href="https://msdn.microsoft.com/f9400597-81bb-44a8-80dc-aba0160aea26">Privilege Constants</a>



<a href="https://msdn.microsoft.com/6e4cae22-23d6-4981-b38c-d298654e59ab">SWbemSecurity.Privileges</a>



<a href="https://msdn.microsoft.com/feaab757-3167-420b-8f42-edced4cd4c53">Scripting API Constants</a>
 

 


---
UID: NF:wmiutils.IWbemPath.GetInfo
title: IWbemPath::GetInfo
author: windows-sdk-content
description: The IWbemPath::GetInfo method returns details about a path that has been placed into a parser object.
old-location: wmi\iwbempath_getinfo.htm
old-project: WmiSdk
ms.assetid: 64f91184-668c-49ec-b8f9-aeeb7227ea6b
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: GetInfo, GetInfo method [Windows Management Instrumentation], GetInfo method [Windows Management Instrumentation],IWbemPath interface, IWbemPath interface [Windows Management Instrumentation],GetInfo method, IWbemPath.GetInfo, IWbemPath::GetInfo, WBEMPATH_INFO_ANON_LOCAL_MACHINE, WBEMPATH_INFO_CIM_COMPLIANT, WBEMPATH_INFO_CONTAINS_SINGLETON, WBEMPATH_INFO_HAS_IMPLIED_KEY, WBEMPATH_INFO_HAS_MACHINE_NAME, WBEMPATH_INFO_HAS_SUBSCOPES, WBEMPATH_INFO_HAS_V2_REF_PATHS, WBEMPATH_INFO_IS_CLASS_REF, WBEMPATH_INFO_IS_COMPOUND, WBEMPATH_INFO_IS_INST_REF, WBEMPATH_INFO_IS_PARENT, WBEMPATH_INFO_IS_SINGLETON, WBEMPATH_INFO_NATIVE_PATH, WBEMPATH_INFO_PATH_HAD_SERVER, WBEMPATH_INFO_SERVER_NAMESPACE_ONLY, WBEMPATH_INFO_V1_COMPLIANT, WBEMPATH_INFO_V2_COMPLIANT, WBEMPATH_INFO_WMI_PATH, _hmm_iwbempath_getinfo, wmi.iwbempath_getinfo, wmiutils/IWbemPath::GetInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmiutils.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WMIQ_ASSOCQ_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemPath.GetInfo
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWbemPath::GetInfo


## -description


The 
<b>IWbemPath::GetInfo</b> method returns details about a path that has been placed into a parser object.


## -parameters




### -param uRequestedInfo [in]

Reserved for future use. Must be 0 (zero).


### -param puResponse [out]

Upon success, this bitmap is set to 0 (zero) or more bits in the following list.



#### WBEMPATH_INFO_ANON_LOCAL_MACHINE

Path has "." or <b>NULL</b> as the server name.



#### WBEMPATH_INFO_HAS_MACHINE_NAME

Server name is specified in the path and that name is not ".".



#### WBEMPATH_INFO_IS_CLASS_REF

There is a class part to the path, but it is not an instance.



#### WBEMPATH_INFO_IS_INST_REF

There is a class part to the path and there are key values.



#### WBEMPATH_INFO_HAS_SUBSCOPES

A subscope is present in the path. Currently WMI does not support scopes.



#### WBEMPATH_INFO_IS_COMPOUND

Compound key is used.



#### WBEMPATH_INFO_HAS_V2_REF_PATHS

One or more keys has a CIM reference.



#### WBEMPATH_INFO_HAS_IMPLIED_KEY

Key names are missing somewhere in the path.



#### WBEMPATH_INFO_CONTAINS_SINGLETON

One or more singletons.



#### WBEMPATH_INFO_V1_COMPLIANT

No scopes and no CIM_REFERENCE keys.



#### WBEMPATH_INFO_V2_COMPLIANT

Reserved. Do not use.



#### WBEMPATH_INFO_CIM_COMPLIANT

Reserved. Do not use.



#### WBEMPATH_INFO_IS_SINGLETON

Object is a singleton.



#### WBEMPATH_INFO_IS_PARENT

Path is just "..".



#### WBEMPATH_INFO_SERVER_NAMESPACE_ONLY

There is no class portion of the path.



#### WBEMPATH_INFO_NATIVE_PATH

Path parser was initialized using 
<a href="https://msdn.microsoft.com/a3ff2aa9-ffa8-4048-ac07-4b815b620d1f">SetText</a>.



#### WBEMPATH_INFO_WMI_PATH

Reserved. Do not use.



#### WBEMPATH_INFO_PATH_HAD_SERVER

Server name was set by either 
<a href="https://msdn.microsoft.com/a3ff2aa9-ffa8-4048-ac07-4b815b620d1f">SetText</a> or 
<a href="https://msdn.microsoft.com/4da66edf-bf38-4246-82fc-27fd14e7d183">SetServer</a>.


## -returns



This method returns one of the following values.




## -see-also




<a href="https://msdn.microsoft.com/71b2597b-d82a-439d-b0b7-af76aefea6a2">IWbemPath</a>
 

 


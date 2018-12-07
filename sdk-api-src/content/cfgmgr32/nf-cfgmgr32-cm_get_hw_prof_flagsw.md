---
UID: NF:cfgmgr32.CM_Get_HW_Prof_FlagsW
title: CM_Get_HW_Prof_FlagsW function
author: windows-sdk-content
description: The CM_Get_HW_Prof_Flags function retrieves the hardware profile-specific configuration flags for a device instance on a local machine.
old-location: devinst\cm_get_hw_prof_flags.htm
tech.root: devinst
ms.assetid: 672a0e4e-f025-4aeb-a865-2a6d6fc1162d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CM_Get_HW_Prof_Flags, CM_Get_HW_Prof_Flags function [Device and Driver Installation], CM_Get_HW_Prof_FlagsA, CM_Get_HW_Prof_FlagsW, cfgmgr32/CM_Get_HW_Prof_Flags, cfgmgr32/CM_Get_HW_Prof_FlagsA, cfgmgr32/CM_Get_HW_Prof_FlagsW, cfgmgrfn_5d158399-60db-47ef-9135-3da047ef7682.xml, devinst.cm_get_hw_prof_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_HW_Prof_FlagsW (Unicode) and CM_Get_HW_Prof_FlagsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Get_HW_Prof_Flags
 - CM_Get_HW_Prof_FlagsA
 - CM_Get_HW_Prof_FlagsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Get_HW_Prof_FlagsW function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.]

The <b>CM_Get_HW_Prof_Flags</b> function retrieves the <a href="https://msdn.microsoft.com/3be5c842-d1b6-4c34-8990-e23e2d08dd23">hardware profile</a>-specific configuration flags for a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device instance</a> on a local machine.


## -parameters




### -param pDeviceID [in]

Pointer to a NULL-terminated string that contains the <a href="https://msdn.microsoft.com/library/Ff541327(v=VS.85).aspx">device instance ID</a> of the device for which to retrieve hardware profile-specific configuration flags.


### -param ulHardwareProfile [in]

A variable of ULONG type that specifies the identifier of the hardware profile for which to retrieve configuration flags. If this parameter is zero, this function retrieves the configuration flags for the current hardware profile. 


### -param pulValue [out]

Pointer to a caller-supplied variable of ULONG type that receives zero or a bitwise OR of the following configuration flags that are defined in <i>Regstr.h</i>:





#### CSCONFIGFLAG_BITS

Bitwise OR of the other CSCONFIGFLAG_Xxx flags.



#### CSCONFIGFLAG_DISABLE

The device instance is disabled in the specified hardware profile.



#### CSCONFIGFLAG_DO_NOT_CREATE

The hardware profile does not support the specified device instance. 



#### CSCONFIGFLAG_DO_NOT_START

The device cannot be started in the specified hardware profile.


### -param ulFlags [in]

Reserved for internal use. Must be set to zero.


##### - pulValue.CSCONFIGFLAG_BITS

Bitwise OR of the other CSCONFIGFLAG_Xxx flags.


##### - pulValue.CSCONFIGFLAG_DISABLE

The device instance is disabled in the specified hardware profile.


##### - pulValue.CSCONFIGFLAG_DO_NOT_CREATE

The hardware profile does not support the specified device instance. 


##### - pulValue.CSCONFIGFLAG_DO_NOT_START

The device cannot be started in the specified hardware profile.


## -returns



If the operation succeeds, <b>CM_Get_HW_Prof_Flags</b> returns CR_SUCCESS. Otherwise, the function returns one of the CR_<i>Xxx</i> error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



To retrieve a list of hardware profile IDs that are currently defined on a local machine, call <a href="https://msdn.microsoft.com/en-us/library/Ff551997(v=VS.85).aspx">SetupDiGetHwProfileList</a>.

To retrieve configuration flags for a device instance on a remote machine, call <a href="https://msdn.microsoft.com/en-us/library/Ff538574(v=VS.85).aspx">CM_Get_HW_Prof_Flags_Ex</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff538574(v=VS.85).aspx">CM_Get_HW_Prof_Flags_Ex</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff551983(v=VS.85).aspx">SetupDiGetHwProfileFriendlyName</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff551997(v=VS.85).aspx">SetupDiGetHwProfileList</a>
 

 


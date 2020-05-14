---
UID: NF:cfgmgr32.CM_Get_HW_Prof_Flags_ExW
title: CM_Get_HW_Prof_Flags_ExW function (cfgmgr32.h)
description: The CM_Get_HW_Prof_Flags_Ex function retrieves the hardware profile-specific configuration flags for a device instance on a remote machine or a local machine.helpviewer_keywords: ["CM_Get_HW_Prof_Flags_Ex","CM_Get_HW_Prof_Flags_Ex function [Device and Driver Installation]","CM_Get_HW_Prof_Flags_ExA","CM_Get_HW_Prof_Flags_ExW","cfgmgr32/CM_Get_HW_Prof_Flags_Ex","cfgmgr32/CM_Get_HW_Prof_Flags_ExA","cfgmgr32/CM_Get_HW_Prof_Flags_ExW","cfgmgrfn_af0f7a15-aa89-49b5-99f9-03f7c1b00a9d.xml","devinst.cm_get_hw_prof_flags_ex"]
old-location: devinst\cm_get_hw_prof_flags_ex.htm
tech.root: devinst
ms.assetid: 660d63b6-b70f-422f-9023-57923290ba47
ms.date: 12/05/2018
ms.keywords: CM_Get_HW_Prof_Flags_Ex, CM_Get_HW_Prof_Flags_Ex function [Device and Driver Installation], CM_Get_HW_Prof_Flags_ExA, CM_Get_HW_Prof_Flags_ExW, cfgmgr32/CM_Get_HW_Prof_Flags_Ex, cfgmgr32/CM_Get_HW_Prof_Flags_ExA, cfgmgr32/CM_Get_HW_Prof_Flags_ExW, cfgmgrfn_af0f7a15-aa89-49b5-99f9-03f7c1b00a9d.xml, devinst.cm_get_hw_prof_flags_ex
f1_keywords:
- cfgmgr32/CM_Get_HW_Prof_Flags_Ex
dev_langs:
- c++
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_HW_Prof_Flags_ExW (Unicode) and CM_Get_HW_Prof_Flags_ExA (ANSI)
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
- CM_Get_HW_Prof_Flags_Ex
- CM_Get_HW_Prof_Flags_ExA
- CM_Get_HW_Prof_Flags_ExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CM_Get_HW_Prof_Flags_ExW function


## -description


<p class="CCE_Message">[This function has been deprecated and should not be used.]

The <b>CM_Get_HW_Prof_Flags_Ex</b> function retrieves the <a href="https://docs.microsoft.com/windows-hardware/drivers/">hardware profile</a>-specific configuration flags for a <a href="https://docs.microsoft.com/windows-hardware/drivers/">device instance</a> on a remote machine or a local machine.


## -parameters




### -param pDeviceID [in]

Pointer to a NULL-terminated string that contains the device instance ID of the device for which to retrieve hardware profile-specific configuration flags.


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


### -param hMachine [in, optional]

A machine handle that is returned by call to <a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a> or <b>NULL</b>. If this parameter is set to <b>NULL</b>, <b>CM_Get_HW_Prof_Flags_Ex</b> retrieves the configuration flags on the local machine.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

##### - pulValue.CSCONFIGFLAG_BITS

Bitwise OR of the other CSCONFIGFLAG_Xxx flags.


##### - pulValue.CSCONFIGFLAG_DISABLE

The device instance is disabled in the specified hardware profile.


##### - pulValue.CSCONFIGFLAG_DO_NOT_CREATE

The hardware profile does not support the specified device instance. 


##### - pulValue.CSCONFIGFLAG_DO_NOT_START

The device cannot be started in the specified hardware profile.


## -returns



If the operation succeeds, <b>CM_Get_HW_Prof_Flags</b> returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



To retrieve a list of the hardware profile IDs that are currently defined on a remote machine, call <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilelistexa">SetupDiGetHwProfileListEx</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa">CM_Get_HW_Prof_Flags</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilefriendlynameexa">SetupDiGetHwProfileFriendlyNameEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilelistexa">SetupDiGetHwProfileListEx</a>
 

 


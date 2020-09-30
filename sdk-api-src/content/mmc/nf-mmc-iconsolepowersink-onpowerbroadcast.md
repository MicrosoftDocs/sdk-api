---
UID: NF:mmc.IConsolePowerSink.OnPowerBroadcast
title: IConsolePowerSink::OnPowerBroadcast (mmc.h)
description: The OnPowerBroadcast method processes WM_POWERBROADCAST notification messages related to the computer's power management.
helpviewer_keywords: ["IConsolePowerSink interface [MMC]","OnPowerBroadcast method","IConsolePowerSink.OnPowerBroadcast","IConsolePowerSink::OnPowerBroadcast","OnPowerBroadcast","OnPowerBroadcast method [MMC]","OnPowerBroadcast method [MMC]","IConsolePowerSink interface","PBT_APMBATTERYLOW","PBT_APMOEMEVENT","PBT_APMPOWERSTATUSCHANGE","PBT_APMQUERYSUSPEND","PBT_APMQUERYSUSPENDFAILED","PBT_APMRESUMEAUTOMATIC","PBT_APMRESUMECRITICAL","PBT_APMRESUMESUSPEND","PBT_APMSUSPEND","_slate_iconsolepowersink_onpowerbroadcast","mmc.iconsolepowersink_onpowerbroadcast","mmc/IConsolePowerSink::OnPowerBroadcast"]
old-location: mmc\iconsolepowersink_onpowerbroadcast.htm
tech.root: mmc
ms.assetid: 69589335-4b80-4f2b-a8d6-74805969c85c
ms.date: 12/05/2018
ms.keywords: IConsolePowerSink interface [MMC],OnPowerBroadcast method, IConsolePowerSink.OnPowerBroadcast, IConsolePowerSink::OnPowerBroadcast, OnPowerBroadcast, OnPowerBroadcast method [MMC], OnPowerBroadcast method [MMC],IConsolePowerSink interface, PBT_APMBATTERYLOW, PBT_APMOEMEVENT, PBT_APMPOWERSTATUSCHANGE, PBT_APMQUERYSUSPEND, PBT_APMQUERYSUSPENDFAILED, PBT_APMRESUMEAUTOMATIC, PBT_APMRESUMECRITICAL, PBT_APMRESUMESUSPEND, PBT_APMSUSPEND, _slate_iconsolepowersink_onpowerbroadcast, mmc.iconsolepowersink_onpowerbroadcast, mmc/IConsolePowerSink::OnPowerBroadcast
req.header: mmc.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConsolePowerSink::OnPowerBroadcast
 - mmc/IConsolePowerSink::OnPowerBroadcast
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IConsolePowerSink.OnPowerBroadcast
---

# IConsolePowerSink::OnPowerBroadcast


## -description

The 
<b>OnPowerBroadcast</b> method processes 
<a href="/windows/desktop/Power/wm-powerbroadcast">WM_POWERBROADCAST</a> notification messages related to the computer's power management.

## -parameters

### -param nEvent [in]

The power broadcast event identifier. The identifier is one of the following values.



#### PBT_APMBATTERYLOW

Battery power is low.



#### PBT_APMOEMEVENT

OEM-defined event occurred.



#### PBT_APMPOWERSTATUSCHANGE

Power status has changed.



#### PBT_APMQUERYSUSPEND

Request for permission to suspend.



#### PBT_APMQUERYSUSPENDFAILED

Suspension request denied.



#### PBT_APMRESUMEAUTOMATIC

Operation resuming automatically after event.



#### PBT_APMRESUMECRITICAL

Operation resuming after critical suspension.



#### PBT_APMRESUMESUSPEND

Operation resuming after suspension.



#### PBT_APMSUSPEND

System is suspending operation.

### -param lParam [in]

Function-specific data. For most events, this parameter is reserved and not used. However, if <i>nEvent</i> is one of the resume events (PBT_APMRESUME*), the <i>lParam</i> parameter can specify the PBTF_APMRESUMEFROMFAILURE flag. This flag indicates that a suspend operation failed after the <a href="/windows/desktop/Power/pbt-apmsuspend">PBT_APMSUSPEND</a> event was broadcast.

### -param plReturn [out]

On return, the snap-in's response to the broadcast event. Generally, set *<i>plReturn</i> to <b>TRUE</b>. The exception is when <i>nEvent</i> is 
<a href="/windows/desktop/Power/pbt-apmquerysuspend">PBT_APMQUERYSUSPEND</a>. To allow the computer suspension to continue in response to the PBT_APMQUERYSUSPEND event, set *<i>plReturn</i> to <b>TRUE</b>; to deny the computer suspension, set *<i>plReturn</i> to BROADCAST_QUERY_DENY. A snap-in that permits computer suspension should perform necessary suspension preparations before returning from this method.

## -returns

If successful, the return value is S_OK. Other return values indicate an error code.

## -see-also

<a href="/windows/desktop/Power/wm-powerbroadcast">WM_POWERBROADCAST</a>
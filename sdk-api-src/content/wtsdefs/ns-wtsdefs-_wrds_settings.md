---
UID: NS:wtsdefs._WRDS_SETTINGS
title: "_WRDS_SETTINGS"
author: windows-driver-content
description: Contains policy-related setting information for a remote session.
old-location: termserv\wrds_settings.htm
old-project: TermServ
ms.assetid: 38AD33F9-F955-4906-90E2-3FE5261A3E58
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "*PWRDS_SETTINGS, PWRDS_SETTINGS, PWRDS_SETTINGS structure pointer [Remote Desktop Services], WRDS_SETTINGS, WRDS_SETTINGS structure [Remote Desktop Services], _WRDS_SETTINGS, termserv.wrds_settings, wtsdefs/PWRDS_SETTINGS, wtsdefs/WRDS_SETTINGS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WRDS_SETTINGS, *PWRDS_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wtsdefs.h
api_name:
-	WRDS_SETTINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WRDS_SETTINGS structure


## -description


Contains policy-related setting information for a remote session.

This structure is used in the <a href="https://msdn.microsoft.com/3680a001-e162-4930-985f-5c50c2e8a8b9">IWRdsProtocolSettings</a> interface and the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method of the <a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a> interface.


## -struct-fields




### -field WRdsSettingType

The category of settings contained (machine group policy, user group policy, or user security accounts manager).


### -field WRdsSettingLevel

The setting level.


### -field WRdsSetting

A structure that contains the policy setting states and values.

A structure that contains the policy setting states and values.


### -field WRdsSetting.switch_is

 


### -field WRdsSetting.switch_is.WRdsSettingLevel

 




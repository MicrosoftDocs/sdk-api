---
UID: NF:wtsprotocol.IWRdsProtocolSettings.GetSettings
title: IWRdsProtocolSettings::GetSettings
author: windows-sdk-content
description: Retrieves the settings for a particular policy.
old-location: termserv\iwrdsprotocolsettings_getsettings.htm
old-project: termserv
ms.assetid: 3a5a7ffd-15e1-4313-ad44-e720cd260f02
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: GetSettings, GetSettings method [Remote Desktop Services], GetSettings method [Remote Desktop Services],IWRdsProtocolSettings interface, IWRdsProtocolSettings interface [Remote Desktop Services],GetSettings method, IWRdsProtocolSettings.GetSettings, IWRdsProtocolSettings::GetSettings, termserv.iwrdsprotocolsettings_getsettings, wtsprotocol/IWRdsProtocolSettings::GetSettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolSettings.GetSettings
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolSettings::GetSettings


## -description


Retrieves the settings for a particular policy.


## -parameters




### -param WRdsSettingType [in]

A value of the <a href="https://msdn.microsoft.com/2B8191F8-FF54-4CF6-9239-F9BFA0FA0A6B">WRDS_SETTING_TYPE</a> enumeration that specifies the area in which to retrieve the settings (machine group policy, user group policy, or user security accounts manager).


### -param WRdsSettingLevel [in]

A value of the <a href="https://msdn.microsoft.com/9E0D754D-4FB4-4878-AA59-33ACFE295651">WRDS_SETTING_LEVEL</a> enumeration that specifies the type of structure contained in the <b>WRdsSetting</b> member of the <a href="https://msdn.microsoft.com/38AD33F9-F955-4906-90E2-3FE5261A3E58">WRDS_SETTINGS</a> structure.


### -param pWRdsSettings [out]

A pointer to a <a href="https://msdn.microsoft.com/38AD33F9-F955-4906-90E2-3FE5261A3E58">WRDS_SETTINGS</a> structure that contains the returned settings.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/3680a001-e162-4930-985f-5c50c2e8a8b9">IWRdsProtocolSettings</a>
 

 


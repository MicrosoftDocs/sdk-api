---
UID: NF:wtsprotocol.IWRdsProtocolSettings.MergeSettings
title: IWRdsProtocolSettings::MergeSettings
author: windows-sdk-content
description: Adds (merges) the specified policy-related settings into the larger group of connection settings.
old-location: termserv\iwrdsprotocolsettings_mergesettings.htm
tech.root: termserv
ms.assetid: fa05bcde-e4db-481b-88ab-57d070153517
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsProtocolSettings interface [Remote Desktop Services],MergeSettings method, IWRdsProtocolSettings.MergeSettings, IWRdsProtocolSettings::MergeSettings, MergeSettings, MergeSettings method [Remote Desktop Services], MergeSettings method [Remote Desktop Services],IWRdsProtocolSettings interface, termserv.iwrdsprotocolsettings_mergesettings, wtsprotocol/IWRdsProtocolSettings::MergeSettings
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolSettings.MergeSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolSettings::MergeSettings


## -description


Adds (merges) the specified policy-related settings into the larger group of connection settings.


## -parameters




### -param pWRdsSettings [in]

A pointer to a <a href="https://msdn.microsoft.com/38AD33F9-F955-4906-90E2-3FE5261A3E58">WRDS_SETTINGS</a> structure that contains the policy-related settings to add.


### -param WRdsConnectionSettingLevel [in]

A value of the <a href="https://msdn.microsoft.com/0D82D26F-1EA6-45A5-90DF-80BE144DC3BF">WRDS_CONNECTION_SETTING_LEVEL</a> enumeration that specifies the type of structure contained in the <b>WRdsConnectionSetting</b> member of the <a href="https://msdn.microsoft.com/9219AE45-5F11-484E-BD78-F8E1AB41D648">WRDS_CONNECTION_SETTINGS</a> structure.


### -param pWRdsConnectionSettings [in, out]

A pointer to a <a href="https://msdn.microsoft.com/9219AE45-5F11-484E-BD78-F8E1AB41D648">WRDS_CONNECTION_SETTINGS</a> structure that contains the existing connection settings. When the method returns, this structure is updated to include the merged settings.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/3680a001-e162-4930-985f-5c50c2e8a8b9">IWRdsProtocolSettings</a>
 

 


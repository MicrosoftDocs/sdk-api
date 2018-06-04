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
 

 


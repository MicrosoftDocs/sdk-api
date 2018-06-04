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
 

 


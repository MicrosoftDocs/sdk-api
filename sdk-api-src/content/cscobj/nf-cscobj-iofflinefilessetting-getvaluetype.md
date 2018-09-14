---
UID: NF:cscobj.IOfflineFilesSetting.GetValueType
title: IOfflineFilesSetting::GetValueType
author: windows-sdk-content
description: Retrieves the data type of a particular Offline Files setting.
old-location: of\iofflinefilessetting_getvaluetype.htm
tech.root: OfflineFiles
ms.assetid: 2b5567bf-a7c6-40b3-ac16-9da805ddb3b3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetValueType, GetValueType method [Offline Files], GetValueType method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],GetValueType method, IOfflineFilesSetting.GetValueType, IOfflineFilesSetting::GetValueType, cscobj/IOfflineFilesSetting::GetValueType, of.iofflinefilessetting_getvaluetype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cscobj.h
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSetting.GetValueType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSetting::GetValueType


## -description


Retrieves the data type of a particular Offline Files setting.


## -parameters




### -param pType [out]

Receives a value from the <a href="https://msdn.microsoft.com/37569197-efd3-4e4e-953a-3bbd2cb07d5a">OFFLINEFILES_SETTING_VALUE_TYPE</a> enumeration that describes the data type of the setting value.


## -returns



S_OK if the scope is returned successfully or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a>
 

 


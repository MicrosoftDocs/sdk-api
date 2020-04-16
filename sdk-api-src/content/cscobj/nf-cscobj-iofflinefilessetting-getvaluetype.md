---
UID: NF:cscobj.IOfflineFilesSetting.GetValueType
title: IOfflineFilesSetting::GetValueType (cscobj.h)
description: Retrieves the data type of a particular Offline Files setting.helpviewer_keywords: ["GetValueType","GetValueType method [Offline Files]","GetValueType method [Offline Files]","IOfflineFilesSetting interface","IOfflineFilesSetting interface [Offline Files]","GetValueType method","IOfflineFilesSetting.GetValueType","IOfflineFilesSetting::GetValueType","cscobj/IOfflineFilesSetting::GetValueType","of.iofflinefilessetting_getvaluetype"]
old-location: of\iofflinefilessetting_getvaluetype.htm
tech.root: offlinefiles
ms.assetid: 2b5567bf-a7c6-40b3-ac16-9da805ddb3b3
ms.date: 12/05/2018
ms.keywords: GetValueType, GetValueType method [Offline Files], GetValueType method [Offline Files],IOfflineFilesSetting interface, IOfflineFilesSetting interface [Offline Files],GetValueType method, IOfflineFilesSetting.GetValueType, IOfflineFilesSetting::GetValueType, cscobj/IOfflineFilesSetting::GetValueType, of.iofflinefilessetting_getvaluetype
f1_keywords:
- cscobj/IOfflineFilesSetting.GetValueType
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesSetting::GetValueType


## -description


Retrieves the data type of a particular Offline Files setting.


## -parameters




### -param pType [out]

Receives a value from the <a href="https://docs.microsoft.com/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_setting_value_type">OFFLINEFILES_SETTING_VALUE_TYPE</a> enumeration that describes the data type of the setting value.


## -returns



S_OK if the scope is returned successfully or an error value otherwise.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessetting">IOfflineFilesSetting</a>
 

 


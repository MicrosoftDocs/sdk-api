---
UID: NF:cscobj.IOfflineFilesCache.GetSettingObject
title: IOfflineFilesCache::GetSettingObject
author: windows-sdk-content
description: Creates an object that represents a particular Offline Files setting.
old-location: of\iofflinefilescache_getsettingobject.htm
tech.root: offlinefiles
ms.assetid: 17b6572d-f05e-4f0e-a247-89acd2963d6b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSettingObject, GetSettingObject method [Offline Files], GetSettingObject method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],GetSettingObject method, IOfflineFilesCache.GetSettingObject, IOfflineFilesCache::GetSettingObject, cscobj/IOfflineFilesCache::GetSettingObject, of.iofflinefilescache_getsettingobject
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
 - IOfflineFilesCache.GetSettingObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesCache::GetSettingObject


## -description


Creates an object that represents a particular Offline Files setting.


## -parameters




### -param pszSettingName [in]

Case-insensitive name of the setting.  One of the following values:


### -param ppSetting [out]

If the setting exists, a pointer to the object's <a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a> interface is returned.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_INVALID_NAME)</code> if the setting name is invalid.




## -remarks



This method is available to both administrators and non-administrators.  Security restrictions are enforced on a setting-by-setting basis.  For example, only administrators can alter a setting that applies to all users on the computer.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 


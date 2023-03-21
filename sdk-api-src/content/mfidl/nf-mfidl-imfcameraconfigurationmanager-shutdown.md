---
UID: NF:mfidl.IMFCameraConfigurationManager.Shutdown
tech.root: 
title: IMFCameraConfigurationManager::Shutdown
ms.date: 08/05/2022
targetos: Windows
description: The IMFCameraConfigurationManager::Shutdown function shuts down the camera configuration manager.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: Windows 11 Build 22621
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFCameraConfigurationManager::Shutdown
f1_keywords:
 - IMFCameraConfigurationManager::Shutdown
 - mfidl/IMFCameraConfigurationManager::Shutdown
dev_langs:
 - c++
helpviewer_keywords:
 - Shutdown
---

## -description

Shuts down the camera configuration manager.

## -remarks

After calling **Shutdown**, subsequent calls to [IMFCameraConfigurationManager::LoadDefaults](nf-mfidl-imfcameraconfigurationmanager-loaddefaults.md) or [IMFCameraConfigurationManager::SaveDefaults](nf-mfidl-imfcameraconfigurationmanager-savedefaults.md) will result in an MF_E_SHUTDOWN error. 


## -see-also


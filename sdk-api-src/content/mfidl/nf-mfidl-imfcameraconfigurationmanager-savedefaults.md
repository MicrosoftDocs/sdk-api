---
UID: NF:mfidl.IMFCameraConfigurationManager.SaveDefaults
tech.root: mf
title: IMFCameraConfigurationManager::SaveDefaults
ms.date: 05/06/2022
targetos: Windows
description: Saves the provided collection of camera control default values. 
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
 - IMFCameraConfigurationManager::SaveDefaults
f1_keywords:
 - IMFCameraConfigurationManager::SaveDefaults
 - mfidl/IMFCameraConfigurationManager::SaveDefaults
dev_langs:
 - c++
helpviewer_keywords:
 - SaveDefaults
---

## -description

Saves the provided collection of camera control default values. 

## -parameters

### -param configurations [in]

An [IMFCameraControlDefaultsCollection](nn-mfidl-imfcameracontroldefaultscollection.md) representing the collection of camera control default values to save.

## -returns

An HRESULT, including the following:

| Value | Description | 
|-------|-------------|
| S_OK | Success. |
| MF_E_SHUTDOWN | The function was called after [IMFCameraConfigurationManager::Shutdown](nf-mfidl-imfcameraconfigurationmanager-shutdown.md) was called. |

## -remarks

The provided default values are assigned to the camera specified with the [MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK](/windows/win32/medfound/mf-devsource-attribute-source-type-vidcap-symbolic-link) value provided when the collection was loaded with a call to [IMFCameraConfigurationManager::LoadDefaults](nf-mfidl-imfcameraconfigurationmanager-loaddefaults.md). Saving an empty collection will clear all existing control default values for the associated camera. 


## -see-also


---
UID: NF:mfidl.IMFCameraConfigurationManager.LoadDefaults
tech.root: mf
title: IMFCameraConfigurationManager::LoadDefaults
ms.date: 05/06/2022
targetos: Windows
description: Loads the camera control defaults for the specified capture source.
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
 - IMFCameraConfigurationManager::LoadDefaults
f1_keywords:
 - IMFCameraConfigurationManager::LoadDefaults
 - mfidl/IMFCameraConfigurationManager::LoadDefaults
dev_langs:
 - c++
helpviewer_keywords:
 - LoadDefaults
---

## -description

Loads the camera control defaults for the specified capture source.

## -parameters

### -param cameraAttributes [in]

A pointer to an [IMFAttributes](../mfobjects/nn-mfobjects-imfattributes.md) in which the [MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK](/windows/win32/medfound/mf-devsource-attribute-source-type-vidcap-symbolic-link) attribute identifies the capture source for which default control values are retrieved.

### -param configurations [out]

Receives a pointer to an [IMFCameraControlDefaultsCollection](nn-mfidl-imfcameracontroldefaultscollection.md) object representing the collection of camera control default values.

## -returns

An HRESULT, including the following:

| Value | Description |
|-------|-------------|
| S_OK | Success |
| MF_E_ATTRIBUTENOTFOUND | The MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK attribute was not found in the IMFAttributes provided in *cameraAttributes* |
| MF_E_SHUTDOWN | The function was called after [IMFCameraConfigurationManager::Shutdown](nf-mfidl-imfcameraconfigurationmanager-shutdown.md) was called. |

## -remarks

If there are no default controls specified, the resulting collection will be empty. I.e.  [IMFCameraControlDefaultsCollection::GetControlCount](nf-mfidl-imfcameracontroldefaultscollection-getcontrolcount.md) will return 0.



## -see-also


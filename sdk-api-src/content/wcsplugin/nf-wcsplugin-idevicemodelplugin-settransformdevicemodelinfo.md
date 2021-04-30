---
UID: NF:wcsplugin.IDeviceModelPlugIn.SetTransformDeviceModelInfo
title: IDeviceModelPlugIn::SetTransformDeviceModelInfo (wcsplugin.h)
description: Provides the plug-in with parameters to determine where in the transform sequence the specific plug-in occurs.
helpviewer_keywords: ["IDeviceModelPlugIn interface [Windows Color System]","SetTransformDeviceModelInfo method","IDeviceModelPlugIn.SetTransformDeviceModelInfo","IDeviceModelPlugIn::SetTransformDeviceModelInfo","SetTransformDeviceModelInfo","SetTransformDeviceModelInfo method [Windows Color System]","SetTransformDeviceModelInfo method [Windows Color System]","IDeviceModelPlugIn interface","_color_IDeviceModelPlugIn::SetTransformDeviceModelInfo","wcs.IDeviceModelPlugIn_SetTransformDeviceModelInfo","wcsplugin/IDeviceModelPlugIn::SetTransformDeviceModelInfo"]
old-location: wcs\IDeviceModelPlugIn_SetTransformDeviceModelInfo.htm
tech.root: WCS
ms.assetid: 01d0815d-1a6b-48f3-9a81-65df0e185e8f
ms.date: 12/05/2018
ms.keywords: IDeviceModelPlugIn interface [Windows Color System],SetTransformDeviceModelInfo method, IDeviceModelPlugIn.SetTransformDeviceModelInfo, IDeviceModelPlugIn::SetTransformDeviceModelInfo, SetTransformDeviceModelInfo, SetTransformDeviceModelInfo method [Windows Color System], SetTransformDeviceModelInfo method [Windows Color System],IDeviceModelPlugIn interface, _color_IDeviceModelPlugIn::SetTransformDeviceModelInfo, wcs.IDeviceModelPlugIn_SetTransformDeviceModelInfo, wcsplugin/IDeviceModelPlugIn::SetTransformDeviceModelInfo
req.header: wcsplugin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeviceModelPlugIn::SetTransformDeviceModelInfo
 - wcsplugin/IDeviceModelPlugIn::SetTransformDeviceModelInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcsPlugIn.h
api_name:
 - IDeviceModelPlugIn.SetTransformDeviceModelInfo
---

# IDeviceModelPlugIn::SetTransformDeviceModelInfo


## -description

Provides the plug-in with parameters to determine where in the transform sequence the specific plug-in occurs.

## -parameters

### -param iModelPosition [in]

The one-based model position of the other device model in the workflow of <i>uiNumModels</i>, as provided in the <a href="/previous-versions/windows/desktop/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize">Initialize</a> function.

### -param pIDeviceModelOther [in]

A pointer to a <b>IDeviceModelPlugIn</b> interface that contains the other device model in the transform sequence.

## -returns

If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.

## -remarks

This function is called by the [CreateMultiProfileTransform](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) function, which is responsible for calling <b>AddRef</b> and <b>Release</b> as appropriate. The function enables plug-in device models to exchange information in a proprietary manner by accessing proprietary plug-in interface functions.

This function will fail if the other device model is a baseline device model, because such models are not plugins and thus inter-plugin communication is not supported.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [IDeviceModelPlugIn](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

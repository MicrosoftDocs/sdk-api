---
UID: NF:photoacquire.IPhotoAcquireSettings.InitializeFromRegistry
title: IPhotoAcquireSettings::InitializeFromRegistry (photoacquire.h)
description: The InitializeFromRegistry method specifies a registry key from which to initialize settings.
helpviewer_keywords: ["IPhotoAcquireSettings interface [Picture Acquisition]","InitializeFromRegistry method","IPhotoAcquireSettings.InitializeFromRegistry","IPhotoAcquireSettings::InitializeFromRegistry","IPhotoAcquireSettingsInitializeFromRegistry","InitializeFromRegistry","InitializeFromRegistry method [Picture Acquisition]","InitializeFromRegistry method [Picture Acquisition]","IPhotoAcquireSettings interface","photoacquire/IPhotoAcquireSettings::InitializeFromRegistry","picacq.iphotoacquiresettings_initializefromregistry"]
old-location: picacq\iphotoacquiresettings_initializefromregistry.htm
tech.root: picacq
ms.assetid: 7459792f-20f8-4449-96c5-8c289b17db68
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],InitializeFromRegistry method, IPhotoAcquireSettings.InitializeFromRegistry, IPhotoAcquireSettings::InitializeFromRegistry, IPhotoAcquireSettingsInitializeFromRegistry, InitializeFromRegistry, InitializeFromRegistry method [Picture Acquisition], InitializeFromRegistry method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::InitializeFromRegistry, picacq.iphotoacquiresettings_initializefromregistry
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
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
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPhotoAcquireSettings::InitializeFromRegistry
 - photoacquire/IPhotoAcquireSettings::InitializeFromRegistry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireSettings.InitializeFromRegistry
---

# IPhotoAcquireSettings::InitializeFromRegistry


## -description

The <code>InitializeFromRegistry</code> method specifies a registry key from which to initialize settings.

## -parameters

### -param pszRegistryKey [in]

Pointer to a null-terminated string containing the registry key.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not yet implemented.

</td>
</tr>
</table>

## -remarks

The structure of the registry has not yet been determined at this point.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings Interface</a>
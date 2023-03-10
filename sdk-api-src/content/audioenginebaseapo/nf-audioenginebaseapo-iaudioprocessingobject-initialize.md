---
UID: NF:audioenginebaseapo.IAudioProcessingObject.Initialize
title: IAudioProcessingObject::Initialize (audioenginebaseapo.h)
description: The Initialize method initializes the APO and supports data of variable length.
helpviewer_keywords: ["IAudioProcessingObject interface [Audio Devices]","Initialize method","IAudioProcessingObject.Initialize","IAudioProcessingObject::Initialize","Initialize","Initialize method [Audio Devices]","Initialize method [Audio Devices]","IAudioProcessingObject interface","audio.iaudioprocessingobject_initialize","audio_syseffects_r_00c2b464-0c56-4357-ab5f-fdcdfb6a2414.xml","audioenginebaseapo/IAudioProcessingObject::Initialize"]
old-location: audio\iaudioprocessingobject_initialize.htm
tech.root: audio
ms.assetid: b73c2e18-ab7b-4e34-9440-f38891f99bf7
ms.date: 12/05/2018
ms.keywords: IAudioProcessingObject interface [Audio Devices],Initialize method, IAudioProcessingObject.Initialize, IAudioProcessingObject::Initialize, Initialize, Initialize method [Audio Devices], Initialize method [Audio Devices],IAudioProcessingObject interface, audio.iaudioprocessingobject_initialize, audio_syseffects_r_00c2b464-0c56-4357-ab5f-fdcdfb6a2414.xml, audioenginebaseapo/IAudioProcessingObject::Initialize
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows Vista and later Windows operating systems.
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
req.lib: Audioenginebaseapo.idl
req.dll: 
req.irql: Any level
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioProcessingObject::Initialize
 - audioenginebaseapo/IAudioProcessingObject::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioenginebaseapo.idl
 - Audioenginebaseapo.idl.dll
api_name:
 - IAudioProcessingObject.Initialize
---

# IAudioProcessingObject::Initialize


## -description

The Initialize method initializes the APO and supports data of variable length.

## -parameters

### -param cbDataSize [in]

This is the size, in bytes, of the initialization data.

### -param pbyData [in]

This is initialization data that is specific to this APO.

## -returns

The <code>Initialize</code> method returns a value of S_OK if the call was successful. Otherwise, this method returns one of the following error codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
APO already initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other HRESULTS</b></dt>
</dl>
</td>
<td width="60%">
These additional error conditions are tracked by the audio engine.

</td>
</tr>
</table>

## -remarks

If this method is used to initialize an APO without the need to initialize any data, it is acceptable to supply a <b>NULL</b> as the value of the pbyData parameter and a 0 (zero) as the value of the cbDataSize parameter. The data that is supplied is of variable length and must have the following format:


```
Struct MyAPOInitializationData
{
APOInitBaseStruct APOInit;
// list additional struct members here
// ...
};
```

## -see-also

<a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitbasestruct">APOInitBaseStruct</a>
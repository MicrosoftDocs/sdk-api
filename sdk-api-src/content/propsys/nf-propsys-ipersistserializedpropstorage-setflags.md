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

# IPersistSerializedPropStorage::SetFlags


## -description


Toggles the property store object between the read-only and read/write state.


## -parameters




### -param flags [in]

Type: <b>PERSIST_SPROPSTORE_FLAGS</b>

The <i>flags</i> parameter takes one of the following values to set options for the behavior of the property storage:



#### FPSPS_DEFAULT (0x00000000)

<b>Windows 7 and later</b>. The property store object is read/write.



#### FPSPS_READONLY (0x00000001)

The property store object is read-only.



#### FPSPS_TREAT_NEW_VALUES_AS_DIRTY (0x00000002)

<b>Introduced in Windows 8</b>. New property values that are added to the property store through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a> method will cause the <a href="https://msdn.microsoft.com/fabafc37-18f2-4def-b6bf-f7daa2bb8f37">IPersistStream::IsDirty</a> method to return S_OK. If this flag is not set, the addition of new property values to the property store does not affect the value returned by <b>IPersistStream::IsDirty</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Read/write is the default setting. <b>IPersistSerializedPropStorage::SetFlags</b> can be called at any time to toggle the read-only and read/write state of the property store.

In versions of Windows before Windows 7, callers can assign a literal zero value directly into the <i>flags</i> parameter to set the read/write state. As of Windows 7, the FPSPS_DEFAULT flag value should be used instead.




---
UID: NF:propsys.IPersistSerializedPropStorage2.GetPropertyStorageBuffer
title: IPersistSerializedPropStorage2::GetPropertyStorageBuffer method
author: windows-driver-content
description: Gets the serialized property storage buffer from the property store instance.
old-location: shell\IPersistSerializedPropStorage2_GetPropertyStorageBuffer.htm
old-project: shell
ms.assetid: a5f349e4-227e-4023-ab80-e8f9fb94dabf
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetPropertyStorageBuffer method [Windows Shell], GetPropertyStorageBuffer method [Windows Shell], IPersistSerializedPropStorage2 interface, GetPropertyStorageBuffer,IPersistSerializedPropStorage2.GetPropertyStorageBuffer, IPersistSerializedPropStorage2, IPersistSerializedPropStorage2 interface [Windows Shell], GetPropertyStorageBuffer method, IPersistSerializedPropStorage2::GetPropertyStorageBuffer, _shell_IPersistSerializedPropStorage2_GetPropertyStorageBuffer, propsys/IPersistSerializedPropStorage2::GetPropertyStorageBuffer, shell.IPersistSerializedPropStorage2_GetPropertyStorageBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPersistSerializedPropStorage2.GetPropertyStorageBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPersistSerializedPropStorage2::GetPropertyStorageBuffer method


## -description


Gets the serialized property storage buffer from the property store instance.


## -parameters




### -param psps [out]

Type: <b>SERIALIZEDPROPSTORAGE*</b>

When this method returns successfully, contains the contents of the property storage buffer.


### -param cb [in]

Type: <b>DWORD</b>

The initial size, in bytes, of the buffer pointed to by <i>psps</i>


### -param pcbWritten [out]

Type: <b>DWORD*</b>

The count of bytes contained in the serialized property storage buffer pointed to by <i>psps</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This methods returns an error if <i>cb</i> is smaller than the total size of the serialized data.

The <b>SERIALIZEDPROPSTORAGE</b> type is defined in Propsys.h as an incomplete type. It should be treated as an array of <b>BYTE</b> values; the format of the returned data is not specified. The contents of the <b>SERIALIZEDPROPSTORAGE</b> structure are suitable for persisting to disk or other storage and can be used to initialize another property store through <a href="https://msdn.microsoft.com/5b6d14ba-3de3-493e-8551-0f3caa02f339">IPersistSerializedPropStorage::SetPropertyStorage</a>.




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

# MFLockDXGIDeviceManager function


## -description


Locks the shared Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager.


## -parameters




### -param pResetToken [out]

Receives a token that identifies this instance of the DXGI Device Manager. Use this token when calling <a href="https://msdn.microsoft.com/D8A2291A-792B-4D24-997A-9C152FFE5426">IMFDXGIDeviceManager::ResetDevice</a>.
          This parameter can be <b>NULL</b>.


### -param ppManager [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function obtains a pointer to a  DXGI Device Manager instance that can be shared between components. The Microsoft Media Foundation platform creates this instance of the  DXGI Device Manager as a singleton object. Alternatively, you can create a new DXGI Device Manager by calling <a href="https://msdn.microsoft.com/5398B6D7-1E7D-4987-A163-3360C805EE9C">MFCreateDXGIDeviceManager</a>.

The first time this function is called, the Media Foundation platform creates the shared DXGI Device Manager. 

When you are done use the <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> pointer, call the <a href="https://msdn.microsoft.com/89121716-4F30-4ACD-AA48-F563550B94A1">MFUnlockDXGIDeviceManager</a>.




## -see-also




<a href="https://msdn.microsoft.com/5398B6D7-1E7D-4987-A163-3360C805EE9C">MFCreateDXGIDeviceManager</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 


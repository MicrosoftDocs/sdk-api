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

# SHGetPropertyStoreForWindow function


## -description


Retrieves an object that represents a specific window's collection of properties, which allows those properties to be queried or set.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window whose properties are being retrieved.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the property store object to retrieve through <i>ppv</i>. This is typically IID_IPropertyStore.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An application can use this function to obtain access to a window's property store so that it can set an explicit Application User Model ID (AppUserModelID) in the <a href="shell.props_System_AppUserModel_Id">System.AppUserModel.ID</a> property.

A window's properties must be removed before the window is closed. If this is not done, the resources used by those properties are not returned to the system. A property is removed by setting it to the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> type VT_EMPTY.

When a call is made to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a> on the object retrieved through <i>ppv</i>, the properties and values are immediately stored on the window. Therefore, no call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a> is needed. No error occurs if it is called, but it has no effect.

An application sets AppUserModelIDs on individual windows to control the application's taskbar grouping and Jump List contents. For instance, a suite application might want to provide a different taskbar button for each of its subfeatures, with the windows relating to that subfeature grouped under that button. Without window-level AppUserModelIDs, those windows would all be grouped together under the main process.

Applications should also use this property store to set these relaunch properties so that the system can return the application to that state.

                

<ul>
<li>
<a href="shell.props_System_AppUserModel_RelaunchCommand">System.AppUserModel.RelaunchCommand</a>
</li>
<li>
<a href="shell.props_System_AppUserModel_RelaunchDisplayNameResource">System.AppUserModel.RelaunchDisplayNameResource</a>
</li>
<li>
<a href="shell.props_System_AppUserModel_RelaunchIconResource">System.AppUserModel.RelaunchIconResource</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>
 

 


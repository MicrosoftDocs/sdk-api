---
UID: NF:shellapi.SHGetPropertyStoreForWindow
title: SHGetPropertyStoreForWindow function (shellapi.h)
description: Retrieves an object that represents a specific window's collection of properties, which allows those properties to be queried or set.helpviewer_keywords: ["SHGetPropertyStoreForWindow","SHGetPropertyStoreForWindow function [Windows Properties]","_shell_SHGetPropertyStoreForWindow","properties.SHGetPropertyStoreForWindow","shell.SHGetPropertyStoreForWindow","shellapi/SHGetPropertyStoreForWindow"]
old-location: properties\SHGetPropertyStoreForWindow.htm
tech.root: properties
ms.assetid: 772aa2c8-6dd1-480c-a008-58f30902cb80
ms.date: 12/05/2018
ms.keywords: SHGetPropertyStoreForWindow, SHGetPropertyStoreForWindow function [Windows Properties], _shell_SHGetPropertyStoreForWindow, properties.SHGetPropertyStoreForWindow, shell.SHGetPropertyStoreForWindow, shellapi/SHGetPropertyStoreForWindow
f1_keywords:
- shellapi/SHGetPropertyStoreForWindow
dev_langs:
- c++
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shell32.dll
- Ext-MS-Win-shell-shell32-l1-2-0.dll
- ext-ms-win-shell-shell32-l1-2-1.dll
- Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
- SHGetPropertyStoreForWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An application can use this function to obtain access to a window's property store so that it can set an explicit Application User Model ID (AppUserModelID) in the <a href="https://docs.microsoft.com/windows/desktop/properties/props-system-appusermodel-id">System.AppUserModel.ID</a> property.

A window's properties must be removed before the window is closed. If this is not done, the resources used by those properties are not returned to the system. A property is removed by setting it to the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> type VT_EMPTY.

When a call is made to <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystore-setvalue">IPropertyStore::SetValue</a> on the object retrieved through <i>ppv</i>, the properties and values are immediately stored on the window. Therefore, no call to <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystore-commit">IPropertyStore::Commit</a> is needed. No error occurs if it is called, but it has no effect.

An application sets AppUserModelIDs on individual windows to control the application's taskbar grouping and Jump List contents. For instance, a suite application might want to provide a different taskbar button for each of its subfeatures, with the windows relating to that subfeature grouped under that button. Without window-level AppUserModelIDs, those windows would all be grouped together under the main process.

Applications should also use this property store to set these relaunch properties so that the system can return the application to that state.

                

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/properties/props-system-appusermodel-relaunchcommand">System.AppUserModel.RelaunchCommand</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/properties/props-system-appusermodel-relaunchdisplaynameresource">System.AppUserModel.RelaunchDisplayNameResource</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/properties/props-system-appusermodel-relaunchiconresource">System.AppUserModel.RelaunchIconResource</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>
 

 


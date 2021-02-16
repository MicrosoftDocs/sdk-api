---
UID: NF:shobjidl_core.IFolderView2.SetViewProperty
title: IFolderView2::SetViewProperty (shobjidl_core.h)
description: Caches a property for an item in the view's property cache.
helpviewer_keywords: ["IFolderView2 interface [Windows Shell]","SetViewProperty method","IFolderView2.SetViewProperty","IFolderView2::SetViewProperty","SetViewProperty","SetViewProperty method [Windows Shell]","SetViewProperty method [Windows Shell]","IFolderView2 interface","_shell_IFolderView2_SetViewProperty","shell.IFolderView2_SetViewProperty","shobjidl_core/IFolderView2::SetViewProperty"]
old-location: shell\IFolderView2_SetViewProperty.htm
tech.root: shell
ms.assetid: 76d91df0-8c90-45dc-9637-910b0874e9fa
ms.date: 12/05/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetViewProperty method, IFolderView2.SetViewProperty, IFolderView2::SetViewProperty, SetViewProperty, SetViewProperty method [Windows Shell], SetViewProperty method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetViewProperty, shell.IFolderView2_SetViewProperty, shobjidl_core/IFolderView2::SetViewProperty
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IFolderView2::SetViewProperty
 - shobjidl_core/IFolderView2::SetViewProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFolderView2.SetViewProperty
---

# IFolderView2::SetViewProperty


## -description

<p class="CCE_Message">[This method is still implemented, but should be considered deprecated as of Windows 7. It might not be implemented in future versions of Windows. It cannot be used with items in search results or library views, so consider using the item's existing properties or, if applicable, emitting properties from your namespace or property handler. See <a href="/windows/desktop/search/-search-3x-wds-extidx-propertyhandlers">Developing Property Handlers for Windows Search</a> for more information.]

Caches a property for an item in the view's property cache.

## -parameters

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A PIDL that identifies the item.

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

The <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> which is to be stored.

### -param propvar [in]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure in which the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> is stored.

## -returns

Type: <b>DEPRECATED_HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

The property is displayed in the view, but not written to the underlying item.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2">IFolderView2</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>



<a href="/windows/desktop/properties/building-property-handlers-property-lists">Property Lists</a>
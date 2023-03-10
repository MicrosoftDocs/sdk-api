---
UID: NF:shobjidl_core.IFolderView2.GetViewProperty
title: IFolderView2::GetViewProperty (shobjidl_core.h)
description: Gets a property value for a given property key from the view's cache.
helpviewer_keywords: ["GetViewProperty","GetViewProperty method [Windows Shell]","GetViewProperty method [Windows Shell]","IFolderView2 interface","IFolderView2 interface [Windows Shell]","GetViewProperty method","IFolderView2.GetViewProperty","IFolderView2::GetViewProperty","_shell_IFolderView2_GetViewProperty","shell.IFolderView2_GetViewProperty","shobjidl_core/IFolderView2::GetViewProperty"]
old-location: shell\IFolderView2_GetViewProperty.htm
tech.root: shell
ms.assetid: 26749aa8-9c5d-4b6b-b5af-bf52d4e8c8ce
ms.date: 12/05/2018
ms.keywords: GetViewProperty, GetViewProperty method [Windows Shell], GetViewProperty method [Windows Shell],IFolderView2 interface, IFolderView2 interface [Windows Shell],GetViewProperty method, IFolderView2.GetViewProperty, IFolderView2::GetViewProperty, _shell_IFolderView2_GetViewProperty, shell.IFolderView2_GetViewProperty, shobjidl_core/IFolderView2::GetViewProperty
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
 - IFolderView2::GetViewProperty
 - shobjidl_core/IFolderView2::GetViewProperty
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
 - IFolderView2.GetViewProperty
---

# IFolderView2::GetViewProperty


## -description

<p class="CCE_Message">[This method is still implemented, but should be considered deprecated as of Windows 7. It might not be implemented in future versions of Windows. It cannot be used with items in search results or library views, so consider using the item's existing properties or, if applicable, emitting properties from your namespace or property handler. See <a href="/windows/desktop/search/-search-3x-wds-extidx-propertyhandlers">Developing Property Handlers for Windows Search</a> for more information.]

Gets a property value for a given property key from the view's cache.

## -parameters

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to an item identifier list (PIDL).

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

The <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> to be retrieved.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure in which the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> is stored.

## -returns

Type: <b>DEPRECATED_HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.

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
Success, the value is in the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The value is not in the view's cache.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2">IFolderView2</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>



<a href="/windows/desktop/properties/building-property-handlers-property-lists">Property Lists</a>
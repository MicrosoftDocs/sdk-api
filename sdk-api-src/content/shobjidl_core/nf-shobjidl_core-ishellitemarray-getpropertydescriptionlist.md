---
UID: NF:shobjidl_core.IShellItemArray.GetPropertyDescriptionList
title: IShellItemArray::GetPropertyDescriptionList (shobjidl_core.h)
description: Gets a property description list for the items in the shell item array.
helpviewer_keywords: ["GetPropertyDescriptionList","GetPropertyDescriptionList method [Windows Shell]","GetPropertyDescriptionList method [Windows Shell]","IShellItemArray interface","IShellItemArray interface [Windows Shell]","GetPropertyDescriptionList method","IShellItemArray.GetPropertyDescriptionList","IShellItemArray::GetPropertyDescriptionList","_shell_IShellItemArray_GetPropertyDescriptionList","shell.IShellItemArray_GetPropertyDescriptionList","shobjidl_core/IShellItemArray::GetPropertyDescriptionList"]
old-location: shell\IShellItemArray_GetPropertyDescriptionList.htm
tech.root: shell
ms.assetid: abedf6a4-dfad-4add-8464-571542b068cb
ms.date: 12/05/2018
ms.keywords: GetPropertyDescriptionList, GetPropertyDescriptionList method [Windows Shell], GetPropertyDescriptionList method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],GetPropertyDescriptionList method, IShellItemArray.GetPropertyDescriptionList, IShellItemArray::GetPropertyDescriptionList, _shell_IShellItemArray_GetPropertyDescriptionList, shell.IShellItemArray_GetPropertyDescriptionList, shobjidl_core/IShellItemArray::GetPropertyDescriptionList
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
 - IShellItemArray::GetPropertyDescriptionList
 - shobjidl_core/IShellItemArray::GetPropertyDescriptionList
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
 - IShellItemArray.GetPropertyDescriptionList
---

# IShellItemArray::GetPropertyDescriptionList


## -description

Gets a property description list for the items in the shell item array.

## -parameters

### -param keyType [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure specifying which property list to retrieve.

### -param riid [in]

Type: <b>REFIID</b>

The IID of the object type to retrieve.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface requested in riid.  This will typically be <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is used to determine a list of properties that are applicable to a set of shell items.  The type of list is specified by a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.  Supported list types include but are not limited to:


<ul>
<li>PKEY_PropList_PreviewDetails </li>
<li>PKEY_PropList_PreviewTitle </li>
<li>PKEY_PropList_FullDetails </li>
<li>PKEY_PropList_TileInfo</li>
<li>PKEY_PropList_ExtendedTileInfo </li>
<li>PKEY_PropList_InfoTip </li>
<li>PKEY_PropList_QuickTip </li>
<li>PKEY_PropList_FileOperationPrompt</li>
<li>PKEY_PropList_ConflictPrompt</li>
<li>PKEY_PropList_SetDefaultsFor</li>
<li>PKEY_PropList_NonPersonal</li>
<li>PKEY_NewMenuPreferredTypes</li>
<li>PKEY_NewMenuAllowedTypes</li>
</ul>
If the shell item array contains more than one item, then this method will obtain an intersection of the properties that would be returned for each item individually.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>



<a href="/windows/desktop/properties/building-property-handlers-property-lists">Property Lists</a>
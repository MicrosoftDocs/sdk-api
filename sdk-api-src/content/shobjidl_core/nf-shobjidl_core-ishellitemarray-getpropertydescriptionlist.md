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

# IShellItemArray::GetPropertyDescriptionList


## -description


Gets a property description list for the items in the shell item array.


## -parameters




### -param keyType [in]

Type: <b>REFPROPERTYKEY</b>

A reference to the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure specifying which property list to retrieve.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the object type to retrieve.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface requested in riid.  This will typically be <a href="https://msdn.microsoft.com/e0530195-27da-4df7-884f-518e905f3c0e">IPropertyDescriptionList</a>.



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is used to determine a list of properties that are applicable to a set of shell items.  The type of list is specified by a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.  Supported list types include but are not limited to:


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




<a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>



<a href="https://msdn.microsoft.com/b7af0491-2ece-42b5-8eea-32643854632f">Property Lists</a>
 

 


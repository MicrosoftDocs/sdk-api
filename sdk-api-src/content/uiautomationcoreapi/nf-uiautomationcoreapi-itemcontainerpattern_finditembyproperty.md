---
UID: NF:uiautomationcoreapi.ItemContainerPattern_FindItemByProperty
title: ItemContainerPattern_FindItemByProperty function (uiautomationcoreapi.h)
description: Retrieves a node within a containing node, based on a specified property value.
helpviewer_keywords: ["ItemContainerPattern_FindItemByProperty","ItemContainerPattern_FindItemByProperty function [Windows Accessibility]","uiauto.uiauto_ItemContainerPattern_FindItemByProperty","uiauto_ItemContainerPattern_FindItemByProperty","uiautomationcoreapi/ItemContainerPattern_FindItemByProperty","winauto.uiauto_ItemContainerPattern_FindItemByProperty"]
old-location: winauto\uiauto_ItemContainerPattern_FindItemByProperty.htm
tech.root: WinAuto
ms.assetid: ffad2cd6-fcf8-436d-888e-1092ba6c3e76
ms.date: 12/05/2018
ms.keywords: ItemContainerPattern_FindItemByProperty, ItemContainerPattern_FindItemByProperty function [Windows Accessibility], uiauto.uiauto_ItemContainerPattern_FindItemByProperty, uiauto_ItemContainerPattern_FindItemByProperty, uiautomationcoreapi/ItemContainerPattern_FindItemByProperty, winauto.uiauto_ItemContainerPattern_FindItemByProperty
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ItemContainerPattern_FindItemByProperty
 - uiautomationcoreapi/ItemContainerPattern_FindItemByProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - ItemContainerPattern_FindItemByProperty
---

# ItemContainerPattern_FindItemByProperty function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves a node within a containing node, based on a specified property value.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The <i>control pattern</i> object.

### -param hnodeStartAfter [in]

Type: <b>HUIANODE</b>

The node after which to start the search.

### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param value [in]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a></b>

The value of the <i>propertyId</i> property.

### -param pFound [out]

Type: <b>HUIANODE*</b>

The node of the matching element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.
---
UID: NF:uiautomationcoreapi.ItemContainerPattern_FindItemByProperty
title: ItemContainerPattern_FindItemByProperty function
author: windows-sdk-content
description: Retrieves a node within a containing node, based on a specified property value.
old-location: winauto\uiauto_ItemContainerPattern_FindItemByProperty.htm
tech.root: WinAuto
ms.assetid: ffad2cd6-fcf8-436d-888e-1092ba6c3e76
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ItemContainerPattern_FindItemByProperty, ItemContainerPattern_FindItemByProperty function [Windows Accessibility], uiauto.uiauto_ItemContainerPattern_FindItemByProperty, uiauto_ItemContainerPattern_FindItemByProperty, uiautomationcoreapi/ItemContainerPattern_FindItemByProperty, winauto.uiauto_ItemContainerPattern_FindItemByProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - ItemContainerPattern_FindItemByProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The property identifier. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a></b>

The value of the <i>propertyId</i> property.


### -param pFound [out]

Type: <b>HUIANODE*</b>

The node of the matching element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




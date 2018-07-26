---
UID: NS:uiautomationclient.ExtendedProperty
title: ExtendedProperty
author: windows-sdk-content
description: Contains information about an extended property.
old-location: winauto\uiauto_extendedproperty.htm
old-project: WinAuto
ms.assetid: 3d0037f5-cff7-4502-b648-a2a60127eaff
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ExtendedProperty, ExtendedProperty structure [Windows Accessibility], uiautomationclient/ExtendedProperty, winauto.uiauto_extendedproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationClient.h
api_name:
 - ExtendedProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ExtendedProperty structure


## -description


Contains information about an extended property. 


## -struct-fields




### -field PropertyName

Type: <b>BSTR</b>

A localized string that contains the name of the extended property.


### -field PropertyValue

Type: <b>BSTR</b>

A string that represents the value of the extended property.   This string should be localized, if appropriate. 


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/D284E4B6-A328-4D79-A95F-DACE00042AF2">IUIAutomationStylesPattern::GetCachedExtendedPropertiesArray</a> and <a href="https://msdn.microsoft.com/AA128739-FB03-4E68-904B-648AE34A175C">GetCurrentExtendedPropertiesArray</a> methods.




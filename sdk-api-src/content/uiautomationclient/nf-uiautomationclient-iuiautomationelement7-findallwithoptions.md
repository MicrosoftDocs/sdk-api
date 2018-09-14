---
UID: NF:uiautomationclient.IUIAutomationElement7.FindAllWithOptions
title: IUIAutomationElement7::FindAllWithOptions
author: windows-sdk-content
description: Find all matching elements in the specified order.
old-location: winauto\uiauto_IUIAutomationElement7_FindAllWithOptions.htm
tech.root: WinAuto
ms.assetid: 1B157EBE-5576-41E8-9B4C-752EFA7832E5
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: FindAllWithOptions, FindAllWithOptions method [Windows Accessibility], FindAllWithOptions method [Windows Accessibility],IUIAutomationElement7 interface, IUIAutomationElement7 interface [Windows Accessibility],FindAllWithOptions method, IUIAutomationElement7.FindAllWithOptions, IUIAutomationElement7::FindAllWithOptions, uiautomationclient/IUIAutomationElement7::FindAllWithOptions, winauto.uiauto_IUIAutomationElement7_FindAllWithOptions, winauto.uiauto_iuiautomationelement_findallwithoptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationElement7.FindAllWithOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationElement7::FindAllWithOptions


## -description


Find all matching elements in the specified order.


## -parameters




### -param arg1

TBD


### -param condition [in]

A pointer to a condition that represents the criteria to match.


### -param arg2

TBD


### -param root [in, optional]

A pointer to the element with which to begin the search.


### -param found

TBD




#### - foundElementsArray [out]

Receives a pointer to an array of matching elements. Returns an empty array if no matching element is found. 


#### - scope

A combination of values specifying the scope of the search.


#### - traversalOptions

Enumeration value specifying the tree navigation order.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/62B3D170-C3B3-48B8-92F8-3DF02F5D4082">IUIAutomationElement7</a>
 

 


---
UID: NF:shdeprecated.IBrowserService2._GetToolbarItem
title: IBrowserService2::_GetToolbarItem method
author: windows-driver-content
description: Deprecated. Gets a specific item from a toolbar.
old-location: shell\IBrowserService2__GetToolbarItem.htm
old-project: shell
ms.assetid: 9bce71ca-189e-4072-9acf-10c8b3a34c5c
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IBrowserService2, IBrowserService2 interface [Windows Shell], _GetToolbarItem method, IBrowserService2::_GetToolbarItem, _GetToolbarItem method [Windows Shell], _GetToolbarItem method [Windows Shell], IBrowserService2 interface, _GetToolbarItem,IBrowserService2._GetToolbarItem, shdeprecated/IBrowserService2::_GetToolbarItem, shell.IBrowserService2__GetToolbarItem, zone_IBrowserService2__GetToolbarItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	IBrowserService2._GetToolbarItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_GetToolbarItem method


## -description


Deprecated. Gets a specific item from a toolbar.


## -parameters




### -param itb [in]

Type: <b>int</b>

The index of the toolbar item to retrieve.


## -returns



Type: <b>LPTOOLBARITEM</b>

A pointer to a <a href="https://msdn.microsoft.com/7378f2f3-c164-46fe-9989-a7a57fceb48a">TOOLBARITEM</a> structure that represents a toolbar item.




## -remarks



This method is implemented by the derived class.



